<template>
  <div>
    <img @click.prevent="play" id="icon" src="/static/play.png"/>
    <audio ref='audio' :src="rainy" loop></audio>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rainy: '/static/rainy.m4a',
      status: false
    }
  },
  watch: {
    status: function (val) {
      let icon = document.getElementById('icon')
      if (val) {
        icon.src = '/static/pause.png'
        this.$refs['audio'].play()
      } else {
        icon.src = '/static/play.png'
        this.$refs['audio'].pause()
      }
    }
  },
  methods: {
    play: function () {
      this.status ? this.status = false : this.status = true
    }
  }
}
</script>

<style lang="less" scoped>
  *{
    margin: 0;
    padding: 0;
  }
  a{
    text-decoration: none;
  }
  body{
    background-image: url("/static/bg.gif");
    background-position: center;
    background-size: auto 100%;
    background-size: cover;
    background-repeat: no-repeat;
    background-color: #020017;
    color: #fff;
    margin: 0;
  }
</style>
