<template>
<transition>
    <div class='user ani'>
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
    left: 20px;
    background-color: #fff;
}
.ani {
  -moz-animation-name: ani-transform-keyframes;
  -moz-animation-duration: 4000ms;
  -moz-animation-delay: 0ms;
  -moz-animation-fill-mode: forwards;
  -moz-animation-timing-function: linear;
  -moz-animation-iteration-count: infinite;
  -moz-transform-origin: 0 0;
  -ms-animation-name: ani-transform-keyframes;
  -ms-animation-duration: 4000ms;
  -ms-animation-delay: 0ms;
  -ms-animation-fill-mode: forwards;
  -ms-animation-timing-function: linear;
  -ms-animation-iteration-count: infinite;
  -ms-transform-origin: 0 0;
  -webkit-animation-name: ani-transform-keyframes;
  -webkit-animation-duration: 4000ms;
  -webkit-animation-delay: 0ms;
  -webkit-animation-fill-mode: forwards;
  -webkit-animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  -webkit-transform-origin: 0 0;
  animation-name: ani-transform-keyframes;
  animation-duration: 4000ms;
  animation-delay: 0ms;
  animation-fill-mode: forwards;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  transform-origin: 0 0;
}
@-moz-keyframes ani-transform-keyframes {
  0% {-moz-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-moz-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  25% {-moz-transform:translate(20px, 10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-moz-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  50% {-moz-transform:translate(30px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-moz-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  75% {-moz-transform:translate(10px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-moz-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  100% {-moz-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);}
}
@-ms-keyframes ani-transform-keyframes {
  0% {-ms-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-ms-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  25% {-ms-transform:translate(20px, 10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-ms-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  50% {-ms-transform:translate(30px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-ms-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  75% {-ms-transform:translate(10px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-ms-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  100% {-ms-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);}
}
@-webkit-keyframes ani-transform-keyframes {
  0% {-webkit-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-webkit-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  25% {-webkit-transform:translate(20px, 10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-webkit-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  50% {-webkit-transform:translate(30px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-webkit-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  75% {-webkit-transform:translate(10px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);-webkit-animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  100% {-webkit-transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);}
}
@keyframes ani-transform-keyframes {
  0% {transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  25% {transform:translate(20px, 10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  50% {transform:translate(30px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  75% {transform:translate(10px, -10px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);animation-timing-function: cubic-bezier(.25,.25,.75,.75);}
  100% {transform:translate(0px, 0px) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) translate(-50%, -50%);}
}html::after { content: url(https://ga-beacon.appspot.com/UA-42910121-1/stylie?pixel); position: absolute; left: -999em; }
</style>
