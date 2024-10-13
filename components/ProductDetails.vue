<template>
  <div class="product-details">
    <img :src="product.bigImage" alt="Product Image" />
    <h1>{{ product.title }}</h1>
    <p>{{ product.description }}</p>
    <p>Price: {{ product.price }}</p>
    <p>In Stock: {{ product.stock }}</p>
    <div>
      <h3>Rating: {{ product.rating }}</h3>
      <div v-for="review in product.reviews" :key="review.id">
        <p>{{ review.comment }}</p>
      </div>
    </div>
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

