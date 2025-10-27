<template>
  <div class="productDetailsSection">
    <div class="imagesSection">
      <div class="smallImagesSection">
        <img src="/product/tshirt.png" alt="" class="smallImg" />
        <img src="/product/tshirt.png" alt="" class="smallImg" />
        <img src="/product/tshirt.png" alt="" class="smallImg" />
      </div>
      <div class="preview">
        <img src="/product/tshirt.png" alt="" class="bigImg" />
      </div>
    </div>
    <div class="textSection">text</div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.productDetailsSection {
  padding: 50px 75px;
  min-width: 100%;
  display: flex;
  gap: 50px;
  justify-content: space-between;
}
.imagesSection {
  display: flex;
  flex: 1;
  gap: 20px;
}
.smallImagesSection {
  display: flex;
  height: 100%;
  flex-direction: column;
  gap: 20px;
}
.textSection {
  flex: 1;
}
.smallImg {
  max-width: 150px;
}
.preview {
  display: flex;
  flex: 1;
}
.bigImg {
  width: 100%;
}
</style>
