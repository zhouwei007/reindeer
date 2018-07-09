<template>
  <div class="myOrder">
    <houseHead>我的订单</houseHead>
    <houseSort :tabList="tabList" @tabClick="tabClick ($event)"></houseSort>
    <div class="content">
      <div v-if="selectedTab.key == 'unComplete'">
        <div class="itemWrap">
          <div class="home-item">
            <div class="item-image"></div>
            <div class="item-des">
              <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
              <div class="price">￥12999.0<span>X2件</span></div>
            </div>
          </div>
          <div class="total">
            <!--<div class="tittle">等待付款</div>-->
            <div class="text">合计：<span style="color: red;">￥25600:00</span></div>
            <div class="set">
              <div class="payBtn">去支付</div>
            </div>
          </div>
        </div>
        <div class="itemWrap">
          <div class="home-item">
            <div class="item-image"></div>
            <div class="item-des">
              <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
              <div class="price">￥12999.0<span>X2件</span></div>
            </div>
          </div>
          <div class="total">
            <div class="text">合计：<span style="color: red;">￥25600:00</span></div>
            <!--<div class="tittle">等待付款</div>-->
            <div class="set">
              <div class="payBtn">去支付</div>
            </div>
          </div>
        </div>
      </div>
      <div v-if="selectedTab.key == 'complete'">
        <div class="itemWrap">
          <div class="home-item">
            <div class="item-image"></div>
            <div class="item-des">
              <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
              <div class="price">￥12999.0<span>X2件</span></div>
            </div>
          </div>
          <div class="total">
            <!--<div class="tittle">等待付款</div>-->
            <div class="text">合计：<span style="color: red;">￥25600:00</span></div>
            <div class="set">
              <div class="payBtn">填写报名信息</div>
            </div>
          </div>
        </div>
      </div>
      <div v-if="selectedTab.key == 'allOrders'">
        <div class="itemWrap">
          <div class="home-item">
            <div class="item-image"></div>
            <div class="item-des">
              <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
              <div class="state">待支付</div>
              <div class="price">￥12999.0<span>X2件</span></div>
            </div>
          </div>
          <div class="total">
            <!--<div class="tittle">等待付款</div>-->
            <div class="text">合计：<span style="color: red;">￥25600:00</span></div>
            <div class="set">
              <div class="payBtn">填写报名信息</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import { mapGetters } from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  import houseSort from './common/house-sort.vue';
  export default{
    template: '.myOrder',
    data: function () {
      return {
        selectedTab:{value: '待支付', key: 'unComplete'},
        tabList:[
          {value: '待支付', key: 'unComplete'},
          {value: '已完成', key: 'complete'},
          {value: '全部订单', key: 'allOrders'}
        ]
      };
    },
    computed: {
    },
    components: { houseHead, houseBtn, houseSort},
    methods: {
      init () {

      },
      tabClick (tab) {
        this.selectedTab = tab;
      }
    },
    mounted: function () {
      this.init()
    }
  };
</script>
<style lang="less">
  @import './../assets/less/myOrder.less';
</style>
