<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <RouterLink :to="`product/${product.id}`">
    <div>
      <img :src="product.image" :alt="product.name" />
      <h3>{{ product.name }}</h3>
      <Rating :value="product.rating" />
      <p>{{ product.price }}</p>
    </div>
  </RouterLink>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
import Rating from './rating.vue'

defineProps<{
  product: {
    id: number
    name: string
    price: string
    image: string
    rating: number
  }
}>()
</script>

<style scoped>
img {
  width: 100%;
  border-radius: 20px;
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
