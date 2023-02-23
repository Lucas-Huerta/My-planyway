<template>
  <h1>
    Index vue
  </h1>
</template>

<script setup>

definePageMeta({
  layout: 'default'
})

let items = null;

let response = await useFetch('metro.json');
items = response;

console.log("items", items);

</script>