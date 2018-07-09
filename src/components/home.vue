<template>
  <div class="myhome">
    <houseHead>驯鹿户外</houseHead>
    <div class="home-item">
      <div class="item-image"></div>
      <div class="item-des">
        <div class="tittle">丝绸之路</div>
        <div class="text">共21场赛事，已有5600人报名</div>
        <div class="btns">
          <div class="introduce" @click="introduce()">路线介绍</div>
          <div class="choice">赛事选择</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { mapGetters } from 'vuex';
import houseBtn from './common/house-btn.vue';
import houseHead from './common/house-head.vue';
export default{
  template: '.myhome',
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
    introduce() {
      this.$router.push('/routerIntroduce');
    }
  },
  mounted: function () {
    this.init()
  }
};
</script>
<style lang="less">
  @import './../assets/less/myhome.less';
</style>
