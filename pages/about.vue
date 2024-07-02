<template>
  <div>
    <h2>About Nuxt Dojo</h2>
    <p>{{ data.message }}</p>
    <p>Nuxt Dojo is a simple e-commerce site built with Nuxt.js.</p>
    <p>It is a project-based learning platform where you can learn Nuxt.js by building a simple e-commerce site.</p>
  </div>  
</template>

<script setup>
  const { data } = await useFetch('http://localhost:3000/api/ditra?name=Mario', {
    method: 'post',
    body: { age: 20 }
  });
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