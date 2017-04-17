<template>
  <div id="app">
    <transition name="fade">
      <div v-if="!isLogin"
           class="login">
        <form class="pure-form">
          输入你的名字来开始：
          <input v-model="name" />
          <select v-model="sex">
            <option>男</option>
            <option>女</option>
          </select>
          <br>
          <button class='pure-button' @click="login">开始！</button>
        </form>
      </div>
    </transition>
    <router-view v-if="isLogin"></router-view>
    <tip v-show="showTip" :text="t"></tip>
  </div>
</template>
<script>
import '@/assets/pure.css'
import tip from '@/components/tip'
import { bus } from '@/bus'

export default {
  name: 'app',
  data () {
    return {
      isLogin: true,
      showTip: false,
      name: '',
      sex: '男',
      t: ''
    }
  },
  components: {
    tip
  },
  mounted: function () {
    this.$cookie.get('name') ? this.isLogin = true : this.isLogin = false
    let th = this
    bus.$on('tip', function (val) {
      th.t = val
      th.showTip = true
      setTimeout(function () {
        th.showTip = false
      }, 3000)
    })
  },
  methods: {
    login: function () {
      this.$cookie.set('name', this.name)
      this.$cookie.set('sex', this.sex)
      this.isLogin = !this.isLogin
      bus.$emit('tip', '欢迎，' + this.name)
    }
  }
}
</script>

<style lang='less'>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #020017;
}

.login {
  position: absolute;
  left: 50%;
  width: 500px;
  height: 80px;
  top: 50%;
  margin-top: -80px;
  margin-left: -250px;
  background: #fff;
  border-radius: 10px;
  color: #000;
  padding: 10px 0;
  button {
    margin: 10px auto;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: margin-top 1.0s, opacity 1.5s;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
  margin-top: 50px;
}
</style>
