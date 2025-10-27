<template>
  <div class="products-section">
    <h2>{{ title }}</h2>
    <div class="products">
      <Product v-for="(product, index) in products" :key="index" :product="product" />
    </div>
    <button>View All</button>
  </div>
</template>

<script setup lang="ts">
import Product from './Product.vue'

defineProps<{
  title: string
  products: Array<{
    id: number
    name: string
    price: string
    image: string
    rating: number
  }>
}>()
</script>

<style scoped>
.products-section {
  padding: 50px 75px;
  background: #f9f9f9;
  display: flex;
  flex-direction: column;
  gap: 50px;
  align-items: center;
}

.products {
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
}

.products-section h2 {
  margin-top: 50px;
  font-size: 48px;
  letter-spacing: -3px;
  font-weight: 900;
  color: rgb(18, 18, 18);
  text-transform: uppercase;
}

button {
  padding: 16px 54px;
  border-radius: 62px;
  display: flex;
  min-width: 218px;
  align-items: center;
  justify-content: center;
  border: none;
}
</style>
