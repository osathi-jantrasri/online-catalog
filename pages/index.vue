<template>   <v-container>     <v-row       dense       align="start"       justify="center"       :wrap="true"     >       <v-col         v-for="product in products"         :key="product.id"         cols="12"         sm="6"         md="4"         lg="3"       >         <v-card>           <v-img :src="product.image" height="200px"></v-img>           <v-card-title>{{ product.title }}</v-card-title>           <v-card-subtitle>             <span>Price: ${{ product.price }}</span>           </v-card-subtitle>           <v-card-subtitle>             <span>In Stock: {{ product.quantity }}</span>           </v-card-subtitle>           <v-card-actions>             <v-btn :to="`/product/${product.id}`" color="primary">View Details</v-btn>           </v-card-actions>         </v-card>       </v-col>     </v-row>   </v-container> </template>

<script>
import ProductCard from '~/components/ProductCard.vue';

export default {
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [{
  "id": 1,
  "title": "First Trust NASDAQ-100- Technology Index Fund",
  "price": "$26.76",
  "stock": 75,
  "image": "http://dummyimage.com/165x100.png/ff4444/ffffff"
}, {
  "id": 2,
  "title": "Sabra Healthcare REIT, Inc.",
  "price": "$147.40",
  "stock": 6,
  "image": "http://dummyimage.com/121x100.png/5fa2dd/ffffff"
}, {
  "id": 3,
  "title": "ProShares UltraShort Nasdaq Biotechnology",
  "price": "$258.23",
  "stock": 33,
  "image": "http://dummyimage.com/245x100.png/dddddd/000000"
}, {
  "id": 4,
  "title": "FlexShares US Quality Large Cap Index Fund",
  "price": "$224.74",
  "stock": 82,
  "image": "http://dummyimage.com/223x100.png/5fa2dd/ffffff"
}, {
  "id": 5,
  "title": "Altisource Residential Corporation",
  "price": "$146.68",
  "stock": 7,
  "image": "http://dummyimage.com/109x100.png/5fa2dd/ffffff"
}, {
  "id": 6,
  "title": "Tower Semiconductor Ltd.",
  "price": "$75.97",
  "stock": 97,
  "image": "http://dummyimage.com/116x100.png/ff4444/ffffff"
}, {
  "id": 7,
  "title": "Synnex Corporation",
  "price": "$138.43",
  "stock": 62,
  "image": "http://dummyimage.com/224x100.png/5fa2dd/ffffff"
}, {
  "id": 8,
  "title": "Xilinx, Inc.",
  "price": "$118.48",
  "stock": 43,
  "image": "http://dummyimage.com/221x100.png/ff4444/ffffff"
}, {
  "id": 9,
  "title": "Catalyst Pharmaceuticals, Inc.",
  "price": "$79.31",
  "stock": 75,
  "image": "http://dummyimage.com/123x100.png/dddddd/000000"
}, {
  "id": 10,
  "title": "XG Technology, Inc",
  "price": "$100.92",
  "stock": 16,
  "image": "http://dummyimage.com/125x100.png/5fa2dd/ffffff"
}],
    };
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
