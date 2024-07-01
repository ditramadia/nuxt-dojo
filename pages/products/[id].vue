<template>
  <div>
    <h2>Product Details</h2>
    <p>Product ID: {{ $route.params.id }}</p>
  </div>  
</template>

<script setup>
  definePageMeta({
    layout: 'products'
  })

  const { id } = useRoute().params;
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