<template>
  <div class="review-section">
    <div class="review-section_header">
      <h2 class="review-section_header-title">Our Happy Customers</h2>
      <div>
        <ArrowLeft :size="28" @click="slidePrevious" />
        <ArrowRight :size="28" @click="slideNext" />
      </div>
    </div>
    <div class="review-container">
      <Review name="Sarah.M" :rating="4" :isVerified="true"
        review="I'm blown away by the quality and style of the clothes I received from Shop.co. From casual wear to elegant dresses, every piece I've bought has exceeded my expectations.”" />
      <Review name="Alex K." :rating="5" :isVerified="true"
        review="Finding clothes that align with my personal style used to be a challenge until I discovered Shop.co. The range of options they offer is truly remarkable, catering to a variety of tastes and occasions.”" />
      <Review name="James L." :rating="5" :isVerified="true"
        review="As someone who's always on the lookout for unique fashion pieces, I'm thrilled to have stumbled upon Shop.co. The selection of clothes is not only diverse but also on-point with the latest trends.”" />
      <Review name="kacem" review="khedma ki zebi" :rating="3" :isVerified="true" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ArrowLeft, ArrowRight } from 'lucide-vue-next';
import Review from './Review.vue';

const slidePrevious = () => {
  console.log("sliding previous");

  const container = document.querySelector('.review-container') as HTMLElement;
  container.scrollLeft -= 400;
};
const slideNext = () => {
  console.log("sliding next");

  const container = document.querySelector('.review-container') as HTMLElement;
  container.scrollLeft += 400;
};

</script>

<style scoped>
.review-section {
  margin-top: 50px;
  padding: 0 75px;
  min-width: 100%;
}

.review-section_header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
}

.review-section_header-title {
  text-align: center;
  font-size: 48px;
  font-weight: 900;
}

svg {
  cursor: pointer;
  border: 1px solid black;
  margin-left: 25px;
}

.review-container {
  display: flex;
  padding: 20px;
  gap: 30px;
  overflow-x: hidden;
  scroll-behavior: smooth;

}
</style>
