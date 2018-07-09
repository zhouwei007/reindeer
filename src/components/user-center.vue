<template>
    <div class="user-center">
      <houseHead>个人中心</houseHead>
      <div class="logo-bg">
        <div class="portrait"></div>
        <div class="name">花花超人</div>
        <div class="jifen">活动积分 ：5000</div>
        <div class="logo-footer">
          <div class="recommend">推荐人 ：花花社</div>
          <div class="qun">群 ：陶冶北京棒</div>
          <div class="gold">淘 金：5000</div>
        </div>
      </div>
      <div class="user-content">
        <div class="part1">
          <div class="content-item">
            <div class="item-logo"></div>
            <div class="item-text">我的订单</div>
            <div class="arrow"></div>
          </div>
          <div class="content-item">
            <div class="item-logo"></div>
            <div class="item-text">我的订单</div>
            <div class="arrow"></div>
          </div>
          <div class="content-item">
            <div class="item-logo"></div>
            <div class="item-text">我的订单</div>
            <div class="arrow"></div>
          </div>
          <div class="content-item">
            <div class="item-logo"></div>
            <div class="item-text">我的订单</div>
            <div class="arrow"></div>
          </div>
        </div>
        <div class="part2"></div>
      </div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseHead from './common/house-head.vue';
  export default {
      template: '.user-center',
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
      components: { houseHead },
      methods: {
        init() {

        },
      },
      mounted: function () {
        this.init()
      }
  };
</script>
<style lang="less" >
    @import './../assets/less/user-center.less';
</style>
