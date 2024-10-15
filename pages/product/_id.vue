<template>
  <div class="product-page">
    <ProductDetails :product="product" />
  </div>
</template>

<script>
import ProductDetails from '~/components/ProductDetails.vue';
import axios from 'axios';

export default {
  components: {
    ProductDetails,
  },
  async asyncData({ params }) {
    try {
      // Fetch the product using the documentId (params.id)
      const response = await axios.get(`http://localhost:1337/api/products?filters[documentId][$eq]=${params.id}`);
      const product = response.data.data[0]; // Assuming the first product matches the documentId

      return { product };
    } catch (error) {
      console.error('Error fetching product:', error);
      return { product: null };
    }
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
