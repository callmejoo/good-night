<template>
    <transition name="fade">
        <div class="tip">{{ text }}</div>
    </transition>
</template>
<script>
export default {
  props: ['text']
}
</script>
<style>
.tip{
    position: absolute;
    top: 30px;
    left: 50%;
    margin-left: -150px;
    width: 300px;
    height: 30px;
    line-height: 30px;
    background-color: #fff;
    border-radius: 10px;
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
