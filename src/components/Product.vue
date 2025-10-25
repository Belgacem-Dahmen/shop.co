<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <img :src="product.image" :alt="product.name" />
    <h3>{{ product.name }}</h3>
    <Rating :value="product.rating" />
    <p>{{ product.price }}</p>
  </div>
</template>

<script setup lang="ts">
import Rating from './rating.vue';

defineProps<{
  product: {
    name: string
    price: string
    image: string
    rating: number
  }
}>()
</script>

<style scoped>
img{
  width: 100%;
  border-radius: 20px;
}
</style>
