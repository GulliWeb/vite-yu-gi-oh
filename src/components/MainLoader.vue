<script>
export default {
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <div class="loader"></div>
</template>

<style scoped>
.loader {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 50px;
  height: 60px;
  color: black;
  display: grid;
}

.loader:before,
.loader:after {
  content: "";
  background:
    linear-gradient(90deg,currentColor calc(100% - 15px),#0000 0) 0 50%/100% 10px,
    conic-gradient(from -136deg at 15px 50%,#0000 ,currentColor 1deg 90deg,#0000 91deg) 35px 0/100% 100%;
  background-repeat: repeat-x;
  animation: l6 1s infinite;
}
.loader:after {
  transform: scaleX(-1);
}
@keyframes l6 {
  80%,100%{background-position: 50px 50%,85px 0}
}
</style>