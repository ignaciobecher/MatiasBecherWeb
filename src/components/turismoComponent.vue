<template>
  <div class="turismo-container">

    <div class="container1" data-aos="zoom-out-up" data-aos-duration="1000">
      <h1 class="h1Title">Turismo Pista</h1>

      <p class="pSubtitle">

      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur,
      voluptatem. Earum, laboriosam possimus rerum nisi ducimus doloremque illo
      voluptatum laborum eveniet temporibus quis consequatur vel, ipsa natus ex.
      Eveniet cum ut eaque soluta cupiditate harum esse?Repellendus nesciunt
      aliquam quaerat expedita impedit, cum optio labore quo totam odit
      accusamus! Error ipsum doloremque possimus alias doloribus maiores. Iure
      officiis vero fugiat? Ipsum cupiditate quidem soluta maiores quaerat
      asperiores eius similique eos rem sequi quod, placeat dolores cum eligendi
      aspernatur doloribus? Nesciunt?
      </p>
    </div>

    <div data-aos="zoom-out-down" data-aos-duration="1000"  class="container2">
      <div class="photoTurism">
        <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img src="/images/turismo1.jpg" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
              <img src="/images/turismo1.jpg" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
              <img src="/images/turismo1.jpg" class="d-block w-100" alt="...">
            </div>
          </div>
          <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
    </div>

    <!-- <img class="photoTurism" src="/images/turismo1.jpg" alt="" /> -->
  </div>
</template>


<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  mounted() {
    AOS.init({
      once: false, // La animación solo se realizará una vez
      offset: 100, // Punto en píxeles antes de que se active la animación
    });

    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      AOS.refreshHard(); // Actualiza la posición de los elementos cuando se hace scroll
    },
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500&display=swap");

* {
  font-family: "Oswald", sans-serif;
}




/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES------------------------ */
@media (min-width: 761px) {
  .turismo-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    background-color: #0b1fba !important;
    color: white;
    padding-top: 30px;
    padding-bottom: 30px;
  }

  .turismo-container .photoTurism {
    width: 100%;
  }

  .container1 p {
    padding: 20px;
    font-size: 20px;
  }

  .container1{
    grid-column: 2;
    grid-row: 1;
  }
  .container2{
    grid-column: 1;
    width: 95%;
    margin: 0 auto;
    align-items: center;
    align-self: center;
    align-content: center;
  }
  


}


/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */

@media (max-width: 760px) {
  .turismo-container {
    background-color: #0b1fba !important;
    padding-top: 30px;
  }

  .h1Title {
    color: white;
    padding-left: 5px;
  }

  .pSubtitle {
    color: white;
    padding-left: 5px;
    padding-right: 5px;
    font-weight: 300;
    line-height: 28px;
  }

  .photoTurism {
    width: 100%;
  }
}
</style>
