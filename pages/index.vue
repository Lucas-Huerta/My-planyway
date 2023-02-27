<template>
  <div id="wrapper-background">
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'default'
})
</script>

<style>
#wrapper-background{
  position: absolute;
  top: 0;
  z-index: -1;
  width: 100vw;
  height: 100vh;
  background-image: url("img/backgroundWrapper.jpg"); 
  background-position: center;
}

.home-pitch-container{
  margin-left: 40px;
  width: 40vw;
  height: 80%;
  justify-content: flex-end;
}

.home-pitch{
  font-size: 20px;
}

.home-pitch-container button{
  width: 40%;
}
</style>