<template>
<transition>
    <div class='user'>
        {{ name }}
    </div>
</transition>
</template>
<script>
export default {
  props: ['name']
}
</script>
<style scoped>
.user{
    position: absolute;
    min-width: 50px;
    min-height: 20px;
    background-color: #fff;
}
</style>
