<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <p>Sign up and get 20% off to your first order <RouterLink to="/"><span>Sign Up Now</span></RouterLink></p>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router';

</script>

<style scoped>
div {
  background: #000;
  color: aliceblue;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 15px 0;
}

p {
  font-size: 14px;
}

span {
  text-decoration: underline;
  font-weight: 900;
}

a {
    color: white;
}
</style>
