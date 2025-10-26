<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="review">
    <Rating :value="rating || 5" :readonly="true" />
    <div class="reviewer-infos">
      <h4 class="review-owner">{{ name }}</h4>
      <span v-if="isVerified" class="review-verified">
        <Check />

      </span>
    </div>

    <p class="review-text">
      "{{ review }}”
    </p>
  </div>
</template>

<script setup lang="ts">
import { Check } from 'lucide-vue-next';
import Rating from './rating.vue';

defineProps<{
  name?: string;
  title?: string;
  rating?: number;
  review?: string;
  isVerified?: boolean
}>();
</script>

<style scoped>
svg {
  width: 16px;
  height: 16px;
}

.review {
  border-radius: 16px;
  border: 1px solid rgb(212, 210, 210);
  padding: 40px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  min-width: 400px;
}

.reviewer-infos {
  display: flex;
  align-items: center;
  gap: 10px;
}

.review-verified {
  background-color: #36cd5e;
  color: white;
  padding: 3px;
  display: flex;
  max-width: fit-content;
  align-items: center;
  justify-content: center;
  border-radius: 50px;
  font-size: 12px;

}
</style>
