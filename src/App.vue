<template>
  <div>
    <Topbar />
    <Navbar />
    <router-view></router-view>
  </div>
</template>

<script setup lang="ts">
import Navbar from './components/Navbar.vue';
import Topbar from './components/Topbar.vue';

</script>

<style scoped></style>
