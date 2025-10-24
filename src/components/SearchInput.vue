<template>
  <div class="search-container">
    <span class="search-icon">
      <Search class="icon" />
    </span>
    <input
      type="text"
      name="search"
      id="search"
      placeholder="Search for products"
    />
  </div>
</template>

<script setup lang="ts">
import { Search } from 'lucide-vue-next'
</script>

<style scoped>
.search-container {
  position: relative;
  width: 100%;
}

.search-icon {
  position: absolute;
  top: 55%;
  left: 14px;
  transform: translateY(-50%);
  color: #a0a0a0;
  
  pointer-events: none;
}

.icon {
  width: 18px;
  height: 18px;
}

input {
  width: 100%;
  border-radius: 62px;
  border: 1px solid #f0f0f0;
  padding: 12px 14px 12px 40px; 
  font-size: 14px;
  outline: none;
  box-sizing: border-box;
  transition: border-color 0.2s, box-shadow 0.2s;
}

input:focus {
  border-color: #a7b5c4;
  box-shadow: 0 0 3px rgba(185, 190, 195, 0.3);
}

input::placeholder {
  color: #b0b0b0;
}
</style>
