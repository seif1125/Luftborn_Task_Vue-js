<template>

  <div class="products-card-grid">
    <product-card v-for="product in products" :product="product" :key="product.id"/>
  </div>

</template>
<script>
import ProductCard from './ProductCard.vue'
export default {
  components: { ProductCard },

  data(){
    return{
        products:[]
    }
  },
mounted(){
    console.log(this.products);
    fetch('https://fakestoreapi.com/products?limit=10')
    .then(res => res.json())
    .then(json => {
        // Handle the JSON data
        console.log(json);
        // Assign the data to a variable or use it as needed
        this.products = json;
        console.log(this.products);
    })
    .catch(error => {
        // Handle errors
        console.error('Error fetching data:', error);
    });

}
}
</script>

<style>

</style>