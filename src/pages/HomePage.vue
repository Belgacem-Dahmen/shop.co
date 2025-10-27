<script setup lang="ts">
import Brands from '../components/Brands.vue'
import DressStyle from '../components/DressStyle.vue'
import ProductSection from '../components/ProductSection.vue'
import ReviewSection from '../components/ReviewSection.vue'
import TopSection from '../components/TopSection.vue'
</script>

<template>
  <TopSection />
  <Brands />
  <ProductSection
    title="New Arrivals"
    :products="[
      {
        id: 1,
        name: 'T-SHIRT WITH TAPE DETAILS',
        price: '$29.99',
        rating: 3.5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 2,
        name: 'SKINNY FIT JEANS',
        price: '$39.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 3,
        name: 'CHECKERED SHIRT',
        price: '$49.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 4,
        name: 'SLEEVE STRIPED T-SHIRT',
        price: '$59.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
    ]"
  />
  <ProductSection
    title="Best Sellers"
    :products="[
      {
        id: 10,
        name: 'Product A',
        price: '$19.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 11,
        name: 'Product B',
        price: '$29.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 12,
        name: 'Product C',
        price: '$39.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
      {
        id: 13,
        name: 'Product D',
        price: '$49.99',
        rating: 5,
        image: 'https://placehold.co/290x295',
      },
    ]"
  />
  <DressStyle />
  <ReviewSection />
</template>

<style scoped>
.main {
  background-color: rgb(203, 192, 192);
}
</style>
