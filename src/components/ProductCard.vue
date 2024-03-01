<template>

    <div class="product-card-container">
         <div class="product-card-canvas">

         </div>
         <div class="product-card-details">
            <div class="product-card-category">
                 <span>
                    {{ product.category}}
                 </span>
                 <img src="../assets/media/combined-shape.svg" alt="options" height="5" width="21">
            </div>
            <div class="price-container">
              <span>{{ product.price }}$</span>
              <div class="title">
                        <p>
                            {{ product.title}}
                        </p>
                  </div>
            </div>
            <div class="product-details">
                  <div class="title">
                        <p>
                            {{ product.title}}
                        </p>
                  </div>
                  <div class="count">
                    <span>inStore</span>
                    <span>{{ product.rating.count }}</span>
                  </div>
            </div>
         </div>
    </div>
  
</template>

<script>
export default {
props:{product:Object},
mounted(){
    console.log(this.product);
}
}
</script>

<style>

</style>