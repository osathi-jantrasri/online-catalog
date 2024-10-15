<template>
  <v-container>
    <v-row dense align="start" justify="center" :wrap="true">
      <v-col
        v-for="product in products"
        :key="product.documentId"
        cols="12"
        sm="6"
        md="4"
        lg="3"
      >
        <!-- Use ProductCard component here -->
        <ProductCard :product="product" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ProductCard from '~/components/ProductCard.vue';
import axios from 'axios';

export default {
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [],
    };
  },
  mounted() {
    this.fetchProducts();
  },
  methods: {
    async fetchProducts() {
      try {
        const response = await axios.get('http://localhost:1337/api/products');
        this.products = response.data.data.map(item => ({
          documentId: item.documentId, // Use documentId as the key
          title: item.title,
          price: item.price,
          stock: item.stock,
          image: item.image,
        }));
      } catch (error) {
        console.error('Error fetching products:', error);
      }
    },
  },
};
</script>

<style scoped>
/* Add your styles here */
</style>
