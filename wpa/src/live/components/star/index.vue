<template>
  <div class="v-star">
    <i class="iconfont icon-star" @click="updateStar(1)" :class="{'active':(starNum >= 1)}"></i>
    <i class="iconfont icon-star" @click="updateStar(2)" :class="{'active':(starNum >= 2)}"></i>
    <i class="iconfont icon-star" @click="updateStar(3)" :class="{'active':(starNum >= 3)}"></i>
    <i class="iconfont icon-star" @click="updateStar(4)" :class="{'active':(starNum >= 4)}"></i>
    <i class="iconfont icon-star" @click="updateStar(5)" :class="{'active':(starNum >= 5)}"></i>
  </div>
</template>
<script>
  import {mapState} from 'vuex';

  export default {
    name: 'v-star',
    props: {

    },
    data() {
      return {
        starNum: 0,
      }
    },
    methods: {
      updateStar(num) {
        this.starNum = num;
        this.$emit('updateStarNum', num);
      }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import 'index.styl';
</style>
