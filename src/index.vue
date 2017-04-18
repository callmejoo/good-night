<template>
  <div>
    <img @click.prevent="play" ref="icon" src="/static/play.png"/>
    <user name="romy"></user>
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
