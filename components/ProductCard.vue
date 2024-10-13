<template>
  <div class="product-card">
    <img :src="product.image" alt="Product Image" />
    <h3>{{ product.title }}</h3>
    <p>Price: {{ product.price }}</p>
    <p>In Stock: {{ product.stock }}</p>
    <nuxt-link :to="`/product/${product.id}`">View Details</nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
