<template>
<div>
    <img @click.prevent="play" ref="icon" src="/static/play.png"/>
    <audio ref="audio" :src="src" loop></audio>
    <div class="name">{{ name }}</div>
</div>
</template>
<script>
export default {
  props: ['name', 'src'],
  data () {
    return {
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
<style scoped>
.name{
  font-size: 5em;
  color: #fff;
  text-shadow: #fff 1px 1px 3px;
}
</style>
