<template>
  <div class="hello">
    <input type="text" v-model="msg" @input="change"/>
    <div>{{getName}}</div>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex';
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '',

    }
  },
  computed : {
    ...mapGetters (['getName'])
  },
  methods:{
    change () {
      this.$store.dispatch('changeName', this.msg)
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
