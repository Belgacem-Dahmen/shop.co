<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="brands">
    <img src="/brands/versace.png" alt="" />
    <img src="/brands/zara.png" alt="" />
    <img src="/brands/gucci.png" alt="" />
    <img src="/brands/prada.png" alt="" />
    <img src="/brands/calvin.png" alt="" />
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
div {
  background: #000;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 20px 75px;
}

img {
  height: 33px;
}

@media screen and (max-width: 675px) {
  .brands {
    display: flex;
    gap: 20px;
  }
  img {
    height: 26px;
  }
}
</style>
