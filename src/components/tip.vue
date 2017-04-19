<template>
    <transition name="fade">
      <div v-show="showTip" class="box">
        <div class="tip">{{ text }}</div>
      </div>
    </transition>
</template>
<script>
export default {
  data () {
    return {
      showTip: false,
      text: ''
    }
  },
  mounted: function () {
    let th = this
    this.$root.$on('tip', function (val) {
      th.text = val
      th.showTip = true
      setTimeout(function () {
        th.showTip = false
      }, 4000)
    })
  }
}

</script>
<style>
.box{
  position: absolute;
  top: 1%;
  text-align: center;
  width: 100%;
  z-index: 5;
}
.tip{
  display: inline-block;
  padding: 0.3em .5em;
  background-color: #fff;
  border-radius: 0.5em;
  min-width: 16em;
}
.fade-enter-active,
.fade-leave-active {
  transition: margin-top 1.0s, opacity 1.5s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
  margin-top: -30px;
}
</style>
