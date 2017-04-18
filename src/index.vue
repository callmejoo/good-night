<template>
  <div>
    <player name="暴雨" src="/static/rainy.m4a"></player>
    <div class="sub">帮助你放松，集中注意力，提升睡眠质量。</div>
    <user name="romy"></user>
    <i class=""
  </div>
</template>

<script>
import user from './components/user'
import player from './components/player'
export default {
  data () {
    return {
    }
  },
  components: {
    user, player
  }
}
</script>

<style scoped>
.sub{
  font-size: 1.5em;
  color:darkgrey
}
</style>
