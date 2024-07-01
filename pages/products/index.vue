<template>
  <div>
    <h2>Products</h2>
    <p>Here are the products available in Nuxt Dojo:</p>
    <p>1. Nuxt.js T-shirt</p>
    <p>2. Nuxt.js Hoodie</p>
    <p>3. Nuxt.js Mug</p>
  </div>  
</template>

<script setup>
  definePageMeta({
    layout: 'products'
  })
</script>

<style scoped>
  h2 {
    margin-bottom: 20px;
    font-size: 36px;
  }

  p {
    margin: 20px 0;
  }
</style>