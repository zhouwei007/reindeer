<template>
    <div class="share-page">
      <houseHead>分享页</houseHead>
      <div class="img-information">
        <div class="logo">
          <div class="logo-text">
            <div class="text">
              花花超人的众筹
            </div>
            <div class="times">
              06月07日 13：56发起
            </div>
          </div>
        </div>
        <div class="portrait"></div>
        <div class="crowdSate">
          <div class="text">众筹即将成功，改购买装备了</div>
          <div class="progress-parent">
            <div class="icon">50%</div>
            <div class="progress-child"></div>
          </div>
          <div class="money">还差12799.99元</div>
        </div>
        <div class="activeInformation">
          <div class="fill-color"></div>
          <div class="last-time">
            <div class="tittle">活动信息</div>
            <div class="time">剩余10天</div>
          </div>
          <div class="home-item">
            <div class="item-image"></div>
            <div class="item-des">
              <div class="tittle">2018第一届驯鹿丝绸路108城市戈壁挑战赛</div>
              <div class="expense">报名费用：<span style="color: red;">9999.00元</span></div>
            </div>
          </div>
        </div>
        <div class="contentClass">
          <houseSort :tabList="tabList" @tabClick="tabClick ($event)" :isCount="isCount"></houseSort>
          <div class="contentPeople">
            <div class="people"></div>
            <div class="people"></div>
            <div class="people"></div>
            <div class="more">
              <div class="text">更多</div>
              <div class="icon">></div>
            </div>
          </div>
          <div class="detailPeople">

          </div>
        </div>
      </div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseHead from './common/house-head.vue';
  import houseSort from './common/house-sort.vue';
  export default {
    template: '.share-page',
    data: function () {
        return {
          tabList:[
            {value: '参赛队伍', key: 'queue'},
            {value: '本队人数', key: 'queuePeople'},
            {value: '支持人数', key: 'supportPeople'},
          ],
          isCount:true
        };
    },
    computed: {},
    components: {houseHead, houseSort},
    methods: {
      init() {

      },
    },
    mounted: function () {
        this.init()
    }
  };
</script>
<style lang="less">
    @import './../assets/less/share-page.less';
</style>
