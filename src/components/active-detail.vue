<template>
    <div class="active-detail">
      <houseHead>活动详情</houseHead>
      <div class="banners">
        <div class="timers">
          <div class="tittle">距开赛</div>
          <div class="text">008天04:36:59</div>
        </div>
        <div class="swiper-container">
          <div class="swiper-wrapper">
            <div class="swiper-slide" v-for="img in listImg" >{{img.url}}</div>
          </div>
          <div class="swiper-pagination swiper-pagination-white"></div>
        </div>
      </div>
      <div class="introduce">
        <div class="top">
          <div class="tittle">首届四天三夜108公里(宁夏)挑战赛</div>
          <div class="pricePlace">
            <div class="price">￥12800.00</div>
            <div class="place">北京市</div>
          </div>
        </div>
        <div class="bottom">
          <div class="item">
            <div class="queenCount">
              <div class="title">
                队伍数量
              </div>
              <div class="text">
                12支
              </div>
            </div>
            <div class="peopleCount">
              <div class="title">
                报名人数
              </div>
              <div class="text">
                200人
              </div>
            </div>
            <div class="support">
              <div class="title">
                支持人数
              </div>
              <div class="text">
                2000人
              </div>
            </div>
          </div>
        </div>
      </div>
      <houseSort :tabList="tabList" @tabClick="tabClick ($event)"></houseSort>
      <div class="content">
        {{selectedTab.value}}
      </div>
      <div class="btns">
        <div class="Crowd" @click="jumpCrowd">我的众筹</div>
        <div class="pay" @click="jumpPay">立即支付</div>
      </div>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseBtn from './common/house-btn.vue';
  import houseHead from './common/house-head.vue';
  import houseSort from './common/house-sort.vue';
  import Swiper from 'swiper';
  import 'swiper/dist/css/swiper.min.css';
  export default {
      template: '.active-detail',
      data: function () {
          return {
            listImg:[
              {
                url:'图片一'
              },
              {
                url:'图片二'
              },
              {
                url:'图片三'
              },
              {
                url:'图片四'
              },
              {
                url:'图片五'
              }
            ],
            tabList: [
              {value: '详情描述', key: 'detail'},
              {value: '报名相关', key: 'sign'},
              {value: '参数标准', key: 'params'},
              {value: '装备要求', key: 'equipment'}
            ],
            selectedTab:{}
          };
      },
      computed: {},
      components: {houseHead, houseBtn, houseSort},
      methods: {
        init() {

        },
        jumpPay () {
          this.$router.push('/payOrder');
        },
        jumpCrowd () {
          this.$router.push('/orderCrowd');
        },
        tabClick (tab) {
            this.selectedTab = tab;
        }
      },
    mounted() {
      console.log('mounted', this)
      var swiper = new Swiper('.swiper-container', {
        pagination: '.swiper-pagination',
        paginationClickable: true,
        loop: true,
        speed: 600,
        autoplay: 4000,
        onTouchEnd: function() {
          swiper.startAutoplay()
        }
      });
    }
  };
</script>
<style lang="less">
    @import './../assets/less/active-detail.less';
</style>
