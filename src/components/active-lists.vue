<template>
    <div class="active-lists">
      <houseHead>活动列表</houseHead>
      <div class="home-item"  @click="jumpActiveDetail">
        <div class="item-image"></div>
        <div class="item-des">
          <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
          <div class="text">2018/05/11~2018/05/14</div>
          <div class="price">￥12999.0</div>
        </div>
        <div class="arrow"></div>
      </div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  export default {
      template: '.active-lists',
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
      computed: {},
      components: {houseBtn, houseHead},
      methods: {
        jumpActiveDetail () {
          this.$router.push('/activeDetail')
        },
        init () {

        }
      },
      mounted: function () {
          this.init()
      }
  };
</script>
<style lang="less">
    @import './../assets/less/active-lists.less';
</style>
