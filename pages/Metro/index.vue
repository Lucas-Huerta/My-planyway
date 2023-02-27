<template>
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
.logoMetro{
  width: 10vw;
  height: 10vh;
}

</style>