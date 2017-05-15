<template>
  <div>
    <app-header></app-header>
    <tabs></tabs>
    <player name="暴雨" src="/static/rainy.m4a"></player>
    <vote></vote>
    <!--<div class="sub">帮助你放松，集中注意力，提升睡眠质量。</div>-->-->
    <!--<user name="romy"></user>-->
  </div>
</template>

<script>
import header from './components/header'
import user from './components/user'
import tabs from './components/tabs'
import player from './components/player'
import vote from './components/vote'
export default {
  data () {
    return {
    }
  },
  components: {
    user,
    player,
    tabs,
    'app-header': header,
    vote
  }
}
</script>

<style scoped>
.sub{
  font-size: 1.5em;
  color:darkgrey
}
</style>
