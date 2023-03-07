<template>
    <div id="metro-wrapper-background">
      <div>
      </div>
      <h1>
        Metro
      </h1>
    </div>
    <div class="flex-col wrapper-metro">
      <h2>
        Choisissez votre ligne 
      </h2>
      <div v-for="index in oneMetro" :key="index">
        {{ index.ligne }}
        <img :src="index.image" class="logoMetro">
      </div>
    </div>
</template>
  
<script setup>
definePageMeta({
  layout: 'default'
})

let items = Object;
let oneMetro = Object;
// let finalMetro = Object;
let response = await useFetch('./metro.json');
items = response;

console.log("items", items);

for (let i = 0; i < items.data.value; i++) {
  oneMetro = items.data.value[i];
  console.log("metro", oneMetro);
}

for (let key in items.data) {
  oneMetro = items.data[key];
  // for (let index in oneMetro) {
  //   finalMetro = oneMetro[index];
  //   console.log(finalMetro);
  // }
}

</script>

<style>

#metro-wrapper-background{
  position: relative;
  top: 0;
  width: 100vw;
  height: 100vh;
}

#metro-wrapper-background div{
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: url("img/metro.png");
  background-position: bottom;
}

#metro-wrapper-background h1{
  font-size: 5em;
  font-weight: lighter;
  margin: 0;
  color: white;
  position: absolute;
  left: 50%;
  margin-left: -100px;
  top: 50%;
  margin-top: -50px;
}

.logoMetro{
  width: 10vw;
  height: 10vh;
}

</style>