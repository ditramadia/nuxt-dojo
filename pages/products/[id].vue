<template>
  <div>
    <h1>{{ product.title }}</h1>
    <p>{{ product.description }}</p>
    <p>{{ product.price }}</p>
    <img :src="product.image" :alt="product.title" />
  </div>  
</template>

<script setup>
  definePageMeta({
    layout: 'products'
  })

  const { id } = useRoute().params;
  const uri = `https://fakestoreapi.com/products/${id}`;
  const { data: product } = await useFetch(uri, { key: id });
</script>