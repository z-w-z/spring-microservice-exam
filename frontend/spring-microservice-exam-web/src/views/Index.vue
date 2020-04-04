<template>
  <div>
    <o-header></o-header>
    <o-main></o-main>
  </div>
</template>

<script>
import OHeader from './common/header'
import OMain from './common/main'
export default {
  data () {
    return {}
  },
  components: {
    OHeader,
    OMain
  }
}
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
  @import "../assets/css/mixin.scss";
  @import "../assets/css/index.scss";
</style>
