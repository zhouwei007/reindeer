<template>
    <div class="strategy">
      <houseHead>攻略</houseHead>
    </div>
</template>
<script>
  import {mapGetters} from 'vuex';
  import houseHead from './common/house-head.vue';
  export default {
      template: '.strategy',
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
<style lang="less">
    @import './../assets/less/strategy.less';
</style>
