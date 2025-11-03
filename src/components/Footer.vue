<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <footer class="footer">
    <div class="contact-section">
      <h2 class="contact-section_header">STAY UP TO DATE ABOUT OUR LATEST OFFERS</h2>
      <div class="contact-section_cta">
        <input type="text" />
        <button>Subscribe to Newsletter</button>
      </div>
    </div>
    <div class="footer-content">
      <div class="footer-col">
        <Logo />
        <p>
          We have clothes that suits your style and which you’re proud to wear. From women to men.
        </p>
        <div>Social icons</div>
      </div>
      <div class="footer-col">
        <p>Company</p>
        <p>About</p>
        <p>Feature</p>
        <p>Feature</p>
        <div>Social icons</div>
      </div>
      <div class="footer-col">
          <p>Help</p>
          <p>Customer Setup</p>
          <p>Delivery Details</p>
          <p>Terms & conditions</p>
          <div>Privacy Policy</div>
      </div>
      <div class="footer-col">
          <p>FAQ</p>
          <p>Account</p>
          <p>Manage Delivery</p>
          <p>Orders</p>
          <p>Payments</p>
      </div>
      <div class="footer-col">
          <p>Ressources</p>
          <p>Free Ebooks</p>
          <p>Dev Tutoriels</p>
          <p>How To</p>
          <p>Youtube Playlist</p>
      </div>
    </div>
    <div>
          <p>Shop.co © 2000-2023, All Rights Reserved</p>
      <div>
        Visa Master card Paypal Apple pay Gpay
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import Logo from './Logo.vue'
</script>

<style scoped>
.footer {
  margin-top: 150px;
  background-color: #f0f0f0;
  color: rgb(2, 2, 2);
  text-align: center;
  padding: 150px 75px 50px 75px ;
  position: relative;
}

.contact-section {
  position: absolute;
  top: 0;
  right: 50%;
  transform: translate(50%, -50%);
  background: #000;
  width: 90%;
  display: flex;
  padding: 32px 32px;
  justify-content: space-between;
  border-radius: 32px;
  align-items: center;
}

.contact-section_header {
  color: white;
  font-size: 40px;
  font-weight: 900;
  max-width: 500px;
  text-align: left;
  line-height: 0.975;
}

.contact-section_cta {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

input {
  padding: 10px 16px;
  border: none;
  border-radius: 62px;
  font-size: 16px;
}

button {
  background: #36cd5e;
  color: white;
  display: flex;
  max-width: fit-content;
  padding: 16px 54px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  border-radius: 62px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 32px;
}

.footer-col {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

@media screen and (max-width : 675px) {
  .contact-section {
    display: flex;
    flex-direction: column;
  }
  
.footer-content {
  margin-top: 50px;
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  
}
}
</style>
