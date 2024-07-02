<template>
  <div class="card">
    <div class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img :src="product.image" alt="Product thumbnail" class="mx-auto my-7" />
      </div>

      <div class="p-7">
        <h2 class="my-7 text-4xl">{{ product.title }}</h2>
        <p class="my-7 text-xl">Price - £{{ price }}</p>
        <h3 class="mb-4 pb-2 border-b-2 font-bold ">Description</h3>
        <p class="mb-7">{{ product.description }}</p>
        <button class="btn flex">
          <i class="material-icons mr-2">add_shopping_cart</i>
          <span>Add to Cart</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
  const { product, rate } = defineProps(['product', 'rate'])
  let price = parseFloat(product.price) * parseFloat(rate)
  price = price.toFixed(2)
</script>

<style scoped>
  img {
    max-width: 400px;
  }
</style>
