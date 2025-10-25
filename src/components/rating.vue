<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="rating-container">
    <div class="stars">
      <template v-for="star in 5" :key="star">
        <!-- Full Star -->
        <svg
          v-if="value >= star"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="#facc15"
          class="star"
        >
          <path
            d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2
               9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
          />
        </svg>

        <!-- Half Star -->
        <svg
          v-else-if="value >= star - 0.5"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          class="star"
        >
          <defs>
            <linearGradient :id="'half' + star" x1="0" x2="1">
              <stop offset="50%" stop-color="#facc15" />
              <stop offset="50%" stop-color="#e5e7eb" />
            </linearGradient>
          </defs>
          <path
            :fill="'url(#half' + star + ')'"
            d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2
               9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
          />
        </svg>

        <!-- Empty Star -->
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="#e5e7eb"
          class="star"
        >
          <path
            d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2
               9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
          />
        </svg>
      </template>
    </div>

    <span class="rating-text">{{ value }}/5</span>
  </div>
</template>

<script setup lang="ts">
interface Props {
  value: number
}

defineProps<Props>()
</script>

<style scoped>
.rating-container {
  display: flex;
  align-items: center;
  font-family: Arial, sans-serif;
}

.stars {
  display: flex;
}

.star {
  width: 24px;
  height: 24px;
  margin-right: 2px;
  transition: fill 0.2s ease-in-out;
}

.rating-text {
  margin-left: 8px;
  color: #333;
  font-size: 16px;
  font-weight: 500;
}
</style>
