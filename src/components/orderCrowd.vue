<template>
    <div class="order-crowd">
      <houseHead>众筹下单</houseHead>
      <div class="relationship">
      <!--  <div class="name">姓名：小超人</div>
        <div class="phone">联系电话：17319232323</div>
        <div class="queue">队伍：呵呵哒</div>-->
        <div class="addRelationship">
          <div class="tittle">新增个人页面<span>></span></div>
          <div class="text">请填写您的个人信息以便工作人员更好的为您服务</div>
        </div>
      </div>
      <div class="itemWrap">
        <div class="home-item">
          <div class="item-image"></div>
          <div class="item-des">
            <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
          </div>
        </div>
        <div class="total">
          <div class="set">
            <div class="text">合计：<span style="color: red;">￥25600:00</span></div>
          </div>
        </div>
      </div>
      <div class="pay">
        <div class="payTittle">众筹支付</div>
        <div class="icon"></div>
      </div>
      <div class="btn" @click="jumpToCrowd">提交订单</div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  export default {
    template: '.order-crowd',
    data: function () {
        return {

        };
    },
    computed: {},
    components: {houseBtn, houseHead},
    methods: {
      init() {

      },
      jumpToCrowd () {
        this.$router.push('/sharePage')
      }
    },
    mounted: function () {
        this.init()
    }
  };
</script>
<style lang="less">
    @import './../assets/less/orderCrowd.less';
</style>
