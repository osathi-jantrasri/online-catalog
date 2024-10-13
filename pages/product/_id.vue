<template>
  <div class="product-page">
    <ProductDetails :product="product" />
  </div>
</template>

<script>
import ProductDetails from '~/components/ProductDetails.vue';

export default {
  components: {
    ProductDetails,
  },
  async asyncData({ params }) {
    const product = {}; // Fetch product by ID from params.id
    return { product };
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
