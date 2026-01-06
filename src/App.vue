<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'

const cart = ref([])
const premium = ref(true)
const updateCart = ()=>{
  cart.value +=1
} 
const removeFromCart =()=>{
  cart.value--
}

</script>
  
<template>
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @remove-item="removeFromCart" @add-to-cart="updateCart"></ProductDisplay>
</template>