<template>
  <div>
    Index vue
  </div>
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