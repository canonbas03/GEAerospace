<script setup>
import { ref } from 'vue'


const var1 = ref(5)
const var2 = ref(8)
const product = ref(null)
const showButtonCh = ref(true)

const showButton = () => {
  product.value = var1.value*var2.value;
  showButtonCh.value = false;

};


</script>

<template>
  <header>Compute Product</header>
  <img src="https://cdn.theforage.com/vinternships/companyassets/ay2tsYxaTif7Nt6z7/AA4Bnq2tJHALwE8cg/1680718790218/pexels-photo-14197334.jpeg" height="200">
  

 

  <div v-if="showButtonCh">
    <button @click="showButton">Calculate</button>
    </div>
  <p v-else>Product is: {{product}}</p>
  
</template>
