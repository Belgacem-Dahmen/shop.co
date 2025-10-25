<template>
  <div class="dressStyleSection">
    <h2>BROWSE BY DRESS STYLE</h2>

    <div class="styleCardsContainer">
      <div class="styleCard ">
        <img src="/dress/casual.png" alt="Casual Dress" />
        <h3>Casual</h3>
      </div>

      <div class="styleCard lg">
        <img src="/dress/formal.png" alt="Formal Dress" />
        <h3>Formal</h3>
      </div>

      <div class="styleCard lg">
        <img src="/dress/party.png" alt="Party Dress" />
        <h3>Party</h3>
      </div>

      <div class="styleCard">
        <img src="/dress/gym.png" alt="Gym Wear" />
        <h3>Gym</h3>
      </div>
    </div>
  </div>
</template>


<script setup lang="ts">

</script>

<style scoped>
.dressStyleSection {
  padding: 0px 75px;
  background-color: #f5f5f5;
  display: flex;
  flex-direction: column;
  text-align: center;
  border-radius: 32px;
  gap: 32px;
}
.dressStyleSection h2 {
  font-size: 48px;
  letter-spacing: -3px;
  font-weight: 900;
  color: #111;
  margin: 48px 0 0 0;
}
.styleCardsContainer {

  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  grid-auto-rows: 330px;
}


.styleCard {

  position: relative;
  background: #fff;
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 2px 10px rgba(0, 0, 0, .06);
  min-height: 150px;
}

/* 2.3 – Image de la carte */
.styleCard img {
  /* On la place en fond visuel, collée à droite */
  position: absolute;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  /* recadrage propre */
  object-position: right center;
  pointer-events: none;
  user-select: none;
  display: block;
}

.styleCard h3 {
  position: absolute;
  top: 14px;
  left: 16px;
  margin: 0;
  font-size: 26px;
  font-weight: 800;
  color: #111;
  z-index: 1;
}

.styleCard.lg {
  grid-column: span 2;

}




@media (max-width: 1024px) {

  /* Tablette : 2 colonnes */
  .styleCardsContainer {
    grid-template-columns: repeat(2, 1fr);
    grid-auto-rows: 170px;
  }

  .styleCard.lg {
    grid-column: span 2;
  }
}

@media (max-width: 600px) {

  /* Mobile : 1 colonne */
  .styleCardsContainer {
    grid-template-columns: 1fr;
    grid-auto-rows: 330px;
  }

  .styleCard,
  .styleCard.lg {
    grid-column: span 1;
  }

  /* chaque tuile = pleine largeur */
  .styleCard img {
    width: 100%;
  }

}
</style>
