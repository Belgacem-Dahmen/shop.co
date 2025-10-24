<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav>
    <Logo />
    <ul class="hide-mobile">
      <li><p>Shop</p></li>
      <li><p>On Sale</p></li>
      <li><p>New Arrivals</p></li>
      <li><p>Brands</p></li>
    </ul>
    <SearchInput class="hide-mobile" />
    <div class="icons">
      <Search class="hide-desktop" />
      <ShoppingCart />
      <UserPen />
    </div>
  </nav>
</template>

<script setup lang="ts">
import { Search, ShoppingCart, UserPen } from 'lucide-vue-next'
import Logo from './Logo.vue'
import SearchInput from './SearchInput.vue'
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-around;
  gap: 40px;
  align-items: center;
  padding: 25px 75px;
}

ul {
  display: flex;
  min-width: max-content;
  gap: 20px;
}

li {
  list-style: none;
}

.icons {
  display: flex;
  gap: 20px;
}

.hide-desktop {
  display: none;
}

@media (max-width: 850px) {
  nav {
    padding: 10px;
  }
  .hide-desktop {
    display: block;
  }
  .hide-mobile {
    display: none;
  }
}
</style>
