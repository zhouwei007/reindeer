<template>
  <div class="house-main-box">
    <router-view></router-view>
    <footer class="house-footer">
      <router-link
        v-for="(item,index) in footers"
        @click="changeTitle(item.content)"
        :key="index"
        :to="{name:item.to}"
        tag="div"
        :class="item.class"
        active-class="on"
      >
        <div class="image"></div>
        <div class="text">{{item.content}}</div>
      </router-link>
    </footer>
  </div>
</template>
<script>
import { mapState } from 'vuex';

export default{
  template: '.house-main-box',
  data () {
    return {
      title: '申请列表',
      footers: [
        {to: 'home', class: 'tab0', content: '首页'},
        {to: 'strategy', class: 'tab1', content: '攻略'},
        {to: 'myCrowd', class: 'tab2', content: '我的众筹'},
        {to: 'myOrder', class: 'tab3', content: '我的订单'}
      ]
    };
  },
  computed: {
    ...mapState([

    ])
  },
  components: {

  },
  methods: {
    changeTitle (t) {
      this.title = t;
      document.title = t;
    }
  }
};
</script>
<style lang="less" scoped>
@import './../../assets/less/main-tab.less';
</style>
