<template>

<div class="dashboard_container">
    <user-section  />
    <products-section :products="products" />
</div>

</template>

<script>
import UserSection from '../components/UserSection.vue'
import ProductsSection from '../components/ProductsSection.vue';

export default {
  components: { UserSection, ProductsSection },
  
  data(){
    return{
        products:[]
    }
  },

mounted(){


}

    
    
    

}
</script>

<style>

</style>