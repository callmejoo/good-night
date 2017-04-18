<template>
<div>
    <audio ref="audio" :src="rainy" loop></audio>
    <div class="name">雨季</div>
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
      let icon = this.$refs['icon']
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
<style>
</style>
