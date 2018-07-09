<template>
  <div class="router-introduce">
    <houseHead>路线介绍</houseHead>
    <div class="content">
      <div class="tittle">行走在敦煌，丝绸之路</div>
      <div class="img"></div>
      <div class="text">敦煌有悠久的历史</div>
    </div>
    <div class="choiceBtn" @click="sign">马上报名</div>
  </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  export default {
      template: '.router-introduce',
      data: function () {
          return {

          };
      },
      computed: {},
      components: {houseBtn, houseHead},
      methods: {
        init() {

        },
        sign(){
          this.$router.push('/activeLists')
        }
      },
      mounted: function () {
          this.init()
      }
  };
</script>
<style lang="less">
    @import './../assets/less/router-introduce.less';
</style>
