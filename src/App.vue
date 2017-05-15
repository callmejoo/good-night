<template>
  <div :class="{bg: isLogin}" id="app">
    <login v-if="!isLogin && showLogin"></login>
    <router-view v-if="isLogin"></router-view>
    <tip></tip>
  </div>
</template>
<script>
import '@/assets/pure.css'
import '@/assets/responsive.css'
import '@/assets/css/font-awesome.min.css'
import login from './components/login'
import tip from '@/components/tip'
export default {
  name: 'app',
  data () {
    return {
      isLogin: false,
      showLogin: false
    }
  },
  components: {
    tip,
    login
  },
  mounted: function () {
    this.$cookie.get('name') ? this.isLogin = true : this.showLogin = true
    let th = this
    this.$root.$on('login', function (val) {
      th.isLogin = val
      th.showLogin = false
    })
  }
}
</script>

<style lang='less'>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.bg{
    height: 100vh;
    background-image: url("/static/bg.gif");
    background-position: center;
    background-size: auto 100%;
    background-size: cover;
    background-repeat: no-repeat;
    color: #000;
    margin: 0;
}
body {
  background-color: #020017;
  overflow: hidden;
  height: 100%;
}
.top{
  position: absolute;
  width: 100%;
  top: 0;
  justify-content: center;
  &.top-1{
    top: 10%;
  }
  &.top-2{
    top: 20%;
  }
  &.top-3{
    top: 30%;
  }
}
</style>
