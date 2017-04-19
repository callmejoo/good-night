<template>
 <transition name="fade">
   <div class="pure-g top top-3">
      <div class="pure-u-2-3 pure-u-md-2-3 pure-u-lg-2-3 pure-u-xl-1-2 login">
        <form class="pure-form">
          <span class="title">关于你？</span>
          <input class="name" v-model="name" placeholder="姓名"/>
          <select class="sex" v-model="sex">
            <option>男</option>
            <option>女</option>
          </select>
          <br>
          <button class='pure-button' @click="login">开始！</button>
        </form>
      </div>
   </div>
  </transition>
</template>
<script>
export default {
  data () {
    return {
      name: '',
      sex: '男'
    }
  },
  methods: {
    login: function () {
      this.$cookie.set('name', this.name)
      this.$cookie.set('sex', this.sex)
      this.$root.$emit('login', true)
      this.$root.$emit('tip', '欢迎，' + this.name)
    }
  }
}
</script>
<<style lang="less" scoped>
.login {
  background: #fff;
  border-radius: 0.8em;
  color: #000;
  padding: .5em .3em;
  .title{
    display: inline-block;
    width: 6em;
    font-size: 1.3em;
  }
}
.name{
  margin: 0.5em 0;
  max-width: 70%;
  display: inline-block!important;
}

.sex{
  max-width: 28%;
  vertical-align: inherit;
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
