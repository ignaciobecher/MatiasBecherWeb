<template>
    <div class="karting-container">

        <p data-aos="fade-right" class="pSubtitle">
        <h1 class="h1Title">Karting</h1>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur, voluptatem. Earum,
        laboriosam possimus rerum nisi ducimus doloremque illo voluptatum laborum eveniet temporibus quis consequatur
        vel, ipsa natus ex. Eveniet cum ut eaque soluta cupiditate harum esse?
        Repellendus nesciunt aliquam quaerat expedita impedit, cum optio labore quo totam odit
        accusamus! Error ipsum doloremque possimus alias doloribus maiores. Iure officiis vero fugiat? Ipsum cupiditate
        quidem soluta maiores quaerat asperiores eius similique eos rem sequi quod, placeat dolores cum eligendi
        aspernatur doloribus? Nesciunt?</p>
        <img data-aos="flip-left" data-aos-duration="3000" data-aos-easing="ease-out-cubic" class="photoKart" src="/images/Kart.jpg" alt="" srcset="">
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
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500&display=swap');

* {
    font-family: 'Oswald', sans-serif;
}

/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES------------------------ */

@media (min-width: 761px) {
    .karting-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr;
        background-color: black;
        color: white;
        padding-top: 30px;
        padding-bottom: 30px;
    }

    .karting-container img {
        width: 100%;
        grid-column: 2;
        grid-row: 1;
        height: 100%;

    }

    .karting-container h1 {
        grid-column: 1;
    }

    .karting-container .pSubtitle {
        grid-column: 1;
        padding: 20px;
        font-size: 20px;
    }
}

/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */

@media (max-width: 760px) {

    .karting-container {
        background-color: black !important;
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
        margin: 0;
    }

    .photoKart {
        width: 100%;
    }
}
</style>