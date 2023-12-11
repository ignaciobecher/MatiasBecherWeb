<template>
    <div class="karting-container">

        <p data-aos="fade-right" class="pSubtitle">
        <h1 class="h1Title">Karting</h1>
        Participo activamente en una vibrante categoría de karting de Cordoba, federada y representativa de 10 provincias de
        todo el país. Este torneo se caracteriza por su alcance nacional y la participación de talentosos pilotos que
        convergen desde distintos rincones de Argentina para competir a un alto nivel. Con la transmisión en vivo vía
        streaming, el campeonato se ha convertido en un espectáculo accesible para aficionados y seguidores, brindando una
        experiencia inmersiva que conecta a la audiencia con la emoción de las carreras.

        En cada fecha, la pista se llena de adrenalina con la presencia de un sólido parque de 45 vehículos, cada uno
        representando la destreza y el ingenio de su piloto. Este año, en particular, la competición ha sido intensa a lo
        largo de 9 emocionantes fechas, llevando el karting a nuevos niveles de emoción y generando expectativas para el
        próximo capítulo de esta apasionante temporada.</p>
        <img data-aos="flip-left" data-aos-duration="3000" data-aos-easing="ease-out-cubic" class="photoKart"
            src="/images/Kart.jpg" alt="" srcset="">
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
}</style>