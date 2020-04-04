<template>
  <div>
    <!-- 主页介绍 -->
    <div id="home">
      <img id="bg" src="../../../static/images/home/index.png" alt="方便好用的考试平台">
      <div id="home-msg">亚洲皇家学府考试专用</div>
      <router-link to="/register" title="免费注册" class="register-now">免费注册</router-link>
    </div>
    <div v-if="isActive" class="go-top-box" @click="goTop(step)">
      <i class="top-icon el-icon-caret-top"></i>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    step: {
      type: Number,
      default: 50
    }
  },
  data () {
    return {
      isActive: false
    }
  },
  methods: {
    // 返回顶部
    goTop: function (i) {
      document.documentElement.scrollTop -= i
      if (document.documentElement.scrollTop > 0) {
        setTimeout(() => this.goTop(i), 16)
      }
    }
  },
  created () {
    let vm = this
    window.onscroll = function () {
      vm.isActive = document.documentElement.scrollTop > 60
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" rel="stylesheet/scss" scoped>
  #home {
    height: 500px;
  }
</style>
