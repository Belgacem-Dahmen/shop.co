<script setup lang="ts">
import Brands from './components/Brands.vue';
import DressStyle from './components/DressStyle.vue';
import Navbar from './components/Navbar.vue';
import ProductSection from './components/ProductSection.vue';
import Topbar from './components/Topbar.vue';
import TopSection from './components/TopSection.vue';
</script>

<template>
  <Topbar />
  <Navbar />
  <TopSection />
  <Brands />
  <ProductSection title="New Arrivals" :products="[
    { name: 'T-SHIRT WITH TAPE DETAILS', price: '$29.99', rating: 3.5, image: 'https://placehold.co/290x295' },
    { name: 'SKINNY FIT JEANS', price: '$39.99', rating: 5, image: 'https://placehold.co/290x295' },
    { name: 'CHECKERED SHIRT', price: '$49.99', rating: 5, image: 'https://placehold.co/290x295' },
    { name: 'SLEEVE STRIPED T-SHIRT', price: '$59.99', rating: 5, image: 'https://placehold.co/290x295' }
  ]" />
  <ProductSection title="Best Sellers" :products="[
    { name: 'Product A', price: '$19.99', rating: 5, image: 'https://placehold.co/290x295' },
    { name: 'Product B', price: '$29.99', rating: 5, image: 'https://placehold.co/290x295' },
    { name: 'Product C', price: '$39.99', rating: 5, image: 'https://placehold.co/290x295' },
    { name: 'Product D', price: '$49.99', rating: 5, image: 'https://placehold.co/290x295' }
  ]" />
  <DressStyle />
</template>

<style scoped>
.main {
  background-color: rgb(203, 192, 192);
}
</style>
