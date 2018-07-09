<template>
  <div class="myCrowd">
    <houseHead>我的众筹</houseHead>
  </div>
</template>
<script>
  import { mapGetters } from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  export default{
    template: '.myCrowd',
    data: function () {
      return {
        errorMessage: '',
        isHide: true,
        titleShow: true,
        dywFinish: false,
        glrFinish: false,
        jkxqFinish: false,
        disabled: true,
        batchApplyId: ''
      };
    },
    computed: {
    },
    components: {
      houseHead,houseBtn
    },
    methods: {
      init () {

      },
    },
    mounted: function () {
      this.init()
    }
  };
</script>
<style lang="less">
  @import './../assets/less/myCrowd.less';
</style>
