<template>
  <div class="footer-container">
    <h1 style="text-align-last: center; color: white;">Contacto</h1>
    <div class="social-container">
      <div class="iconDiv">
        <a href="https://es-la.facebook.com/mati.becher/" target="_blank">
          <i class="bi bi-facebook"></i>
        </a>
      </div>

      <div class="iconDiv">
        <a href="https://www.instagram.com/matibecher_/" target="_blank">
          <i class="bi bi-instagram"></i>
        </a>
      </div>

      <div class="iconDiv">
        <a href="https://wa.link/7he26a" target="_blank">
          <i class="bi bi-whatsapp"></i>
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

/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES----------------------------- */

@media (min-width: 761px){
  .footer-container {
    background-color: #0b1fba !important;
  }

  .social-container {
    display: grid;
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr 1fr;
    justify-content: center;
    /* Centra horizontalmente */
    ;
    padding-top: 30px;
    padding-bottom: 30px;
  }

  .iconDiv {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .iconDiv i {
    font-size: 30px;
    color: white;
    transform: rotate(0deg);
    transition-duration: 250ms;
  }

  .iconDiv i:hover{
    color: black;
    transform: rotate(360deg);
  }
  
}


/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS----------------------------- */

@media (max-width: 760px) {
  .footer-container {
    background-color: #0b1fba !important;
  }

  .social-container {
    display: grid;
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr 1fr;
    justify-content: center;
    /* Centra horizontalmente */
    ;
    padding-top: 30px;
    padding-bottom: 30px;
  }

  .iconDiv {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .iconDiv i {
    font-size: 30px;
    color: white;
  }
}
</style>
