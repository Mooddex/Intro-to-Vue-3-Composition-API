<script setup>
import { ref } from 'vue'

const product = ref('Socks')
const url = ref('https://placecats.com/300/200')

</script>

<template>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">
        <!-- image goes here -->
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <img :src="url" :alt="CatImage">
        <a :href="url">link to image</a>
      </div>
    </div>
  </div>
</template>