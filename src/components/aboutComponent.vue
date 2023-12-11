<template>
    <div class="about-container">
       
        <p data-aos="fade-right" class="pSubtitle">
            <h1 class="h1Title">Matias Becher</h1>
            Matías Becher, con sus 27 años de edad y origen en Villa Mercedes (San Luis), ha forjado una destacada carrera deportiva de 9 años como piloto. Durante este tiempo, ha alcanzado la cima con la victoria en 2 campeonatos, se ha destacado como subcampeón en una ocasión y ha demostrado su consistencia con una amplia presencia en podios, consolidándose como una figura prominente en el mundo del automovilismo.</p>
        <img data-aos="fade-right" src="/images/aboutPhoto.jpeg" alt="" class="photoAbout">

    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  mounted() {
    AOS.init({
      once: true, // La animación solo se realizará una vez
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
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500&display=swap');

* {
    font-family: 'Oswald', sans-serif;
}

/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES ------------------------ */
@media (min-width: 761px) {
    .about-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto auto;
        background-color: #0b1fba !important;
        padding-top: 30px;
        padding-bottom: 30px;
        color: white;
    }

    .about-container h1 {
        grid-row: 2;
        grid-column: 2;
    }

    .about-container p {
        grid-row: 2;
        grid-column: 2;
        padding: 20px;
        font-size: 20px;
    }

    .about-container img {
        width: 100%;
        grid-row: 2;
        grid-column: 1;
    }
}

/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */
@media (max-width: 760px) {
    .about-container {
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
    }

    .photoAbout {
        width: 100%;
    }
}
</style>
