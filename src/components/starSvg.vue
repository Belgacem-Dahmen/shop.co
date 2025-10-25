<template>
  <svg
    :width="width"
    :height="width"
    viewBox="0 0 104 104"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    :style="computedStyle"
  >
    <path
      d="M52 0C53.7654 27.955 76.0448 50.2347 104 52C76.0448 53.7654 53.7654 76.0448 52 104C50.2347 76.0448 27.955 53.7654 0 52C27.955 50.2347 50.2347 27.955 52 0Z"
      :fill="color"
    />
  </svg>
</template>

<script setup lang="ts">
import { computed } from 'vue'

interface Props {
  width?: number | string
  color?: string
  top?: string
  left?: string
  right?: string
  bottom?: string
  zIndex?: number
}

const props = defineProps<Props>()

const computedStyle = computed(() => ({
  position: 'absolute',
  top: props.top,
  left: props.left,
  right: props.right,
  bottom: props.bottom,
  zIndex: props.zIndex ?? 1,
}))
</script>

<style scoped>
svg {
  position: absolute;
}
</style>
