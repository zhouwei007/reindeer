<template>
    <div class="pay-order">
      <houseHead>自付下单</houseHead>
      <div class="relationship">
        <div class="name">姓名：小超人</div>
        <div class="phone">联系电话：17319232323</div>
        <div class="queue">队伍：呵呵哒</div>
      </div>
      <div class="active">
        <div class="img"></div>
        <div class="tittle">成戈3，为城市荣耀而战</div>
        <div class="price">
          <div class="onePrice">￥12800.00</div>
          <div class="count">X1</div>
        </div>
      </div>
      <div class="computed">
        <div class="computedCount">
          <div class="reduce">-</div>
          <div class="count">2</div>
          <div class="plus">+</div>
        </div>
        <div class="totalPrice">
          合计:￥12800.00
        </div>
      </div>
      <div class="pay">
        <div class="payTittle">在线支付</div>
        <div class="icon"></div>
      </div>
      <div class="btn" @click="jumpToOrder">提交订单</div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  export default {
      template: '.pay-order',
      data: function () {
          return {

          };
      },
      computed: {},
      components: {houseBtn, houseHead },
      methods: {
        init() {

        },
        jumpToOrder () {
          this.$router.push('/main/myOrder')
        }
      },
      mounted: function () {
          this.init()
      }
  };
</script>
<style lang="less">
    @import './../assets/less/pay-order.less';
</style>
