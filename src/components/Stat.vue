<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>

    <p class="stat-number">{{ number }}+</p>
    <p class="stat-title">{{ title }}</p>

  </div>
</template>

<script setup lang="ts">
defineProps<{
  number: string
  title: string
}>()
</script>

<style scoped>
.stat-number {
  font-size: 48px;
  font-weight: 900;
  margin: 0;
  color: rgb(18, 18, 18) !important;
}

p {
  color: rgb(18, 17, 17, 0.60);
  font-size: 16px;
}
</style>
