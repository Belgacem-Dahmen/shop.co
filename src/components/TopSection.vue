<template>
  <section class="topSection">
    <StarSvg width="80" color="#000" top="100px" right="30px" />
    <StarSvg width="60" color="#000" top="320px" right="600px" />
    <div class="topSection_content">
      <h1>FIND CLOTHES THAT MATCHES YOUR STYLE</h1>
      <p>Browse through our diverse range of meticulously crafted garments, designed to bring out your individuality and
        cater to your sense of style.</p>
      <button>Shop Now</button>
      <div class="topSection_content-stats">
        <Stat number="200" title="International Brands" />
        <Stat number="2,000" title="High-Quality Products" />
        <Stat number="30,000" title="Happy Customers" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import StarSvg from './starSvg.vue';
import Stat from './Stat.vue';
</script>

<style scoped>
.topSection {
  min-height: 750px;
  display: flex;
  align-items: center;
  background-image: url('../../public/image.png');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  padding: 0 75px;
  position: relative;
}

.topSection_content h1 {
  font-size: 74px;
  font-weight: 900;
  line-height: 1.1;
  letter-spacing: -4px;
  padding-right: 20px;
  line-height: 64px;

}

.topSection_content {
  display: flex;
  flex-direction: column;
  gap: 30px;
  height: 100%;
  max-width: 600px;
  color: rgb(18, 17, 17);

}

.topSection_content p {
  color: rgb(18, 17, 17, 0.60);
  font-size: 16px;
}

button {
  background: #000;
  color: white;
  display: flex;
  max-width: fit-content;
  padding: 16px 54px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  border-radius: 62px;
}

.topSection_content-stats {
  display: flex;
  gap: 30px;
}
</style>
