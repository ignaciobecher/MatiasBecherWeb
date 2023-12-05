<template>
  <div class="footer-container">
    <div class="social-container">
      <div class="iconDiv">
        <a href="">
          <i class="bi bi-facebook"></i>
        </a>
      </div>

      <div class="iconDiv">
        <a href="">
          <i class="bi bi-instagram"></i>
        </a>
      </div>

      <div class="iconDiv">
        <a href="">
          <i class="bi bi-youtube"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500&display=swap");

* {
  font-family: "Oswald", sans-serif;
}

.footer-container {
  background-color: #0b1fba !important;
}

.social-container {
  display: grid;
  grid-template-rows: auto;
  grid-template-columns: 1fr 1fr 1fr;
  justify-content: center; /* Centra horizontalmente */;
  padding-top: 30px;
  padding-bottom: 30px;
}

.iconDiv {
  display: flex;
  align-items: center;
  justify-content: center;
}

.iconDiv i{
    font-size: 30px;
    color: white;
}
</style>
