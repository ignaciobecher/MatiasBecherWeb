<template>
  <div class="history-container">
    <h1 data-aos="zoom-in-right" data-aos-duration="1000" class="h1Title">Propuesta publicitaria</h1>

    <p data-aos="zoom-in-right" data-aos-duration="1000" class="pSubtitle">
    ¡Le ofrecemos un plan completo para darle visibilidad a su empresa de manera impactante! <br>

    1. Anuncios en Autos y Kartings:
     Colocaremos su logo en 2 autos de carreras y 2 kartings para que destaque en eventos emocionantes.<br>
    2. Publicidad en Instagram (Anuncio Pagado):
     Llegaremos directamente a más personas a través de publicidad en nuestro Instagram.<br>
    3. Ropa de Competición con su Marca:
     Su marca estará presente en la ropa que usamos en las competiciones, destacándose en acción. También, ofrecemos la
    opción de utilizar su propia indumentaria y merchandising para una mayor identificación.<br>


    4. Equipo de Promotores:
    Contrate a nuestro equipo de promotores según su conveniencia en cada evento.<br>


    5. Espacio en mi Página Web:
     Tendrá una sección exclusiva en mi página web para mostrar su marca.<br>


    6. Apariciones en Medios:
     Apareceremos en más de 10 medios de comunicación cada mes, dentro y fuera de San Luis.<br>


    7. Conferencias de Prensa:
     Participaremos en al menos 5 conferencias de prensa al año, llevando su marca a diferentes lugares.<br>


    8. Presencia Internacional en Paraguay:
    - Su marca será destacada en una conferencia y medios de prensa en Paraguay, alcanzando audiencias internacionales.<br>


    9. Contacto Diario con Miles de Personas:
    - Acceso directo a más de 5000 personas diarias a través de nuestras asociaciones.<br>


    10. Destaque en Redes Socialesn>:
     Su marca será destacada en mi perfil de Instagram con más de 100,000 vistas al mes, y con un crecimiento diario
    significativo.<br>


    
    11. Sorteo Especial para Seguidores:
    - Realizaremos un sorteo para atraer más seguidores y amor hacia su marca.<br>


    12. Reporte Mensual de Resultados:
     Le proporcionaremos un reporte mensual que le mostrará cuántas personas han visto su marca en nuestras actividades.<br><br>


    Elija las opciones que se adapten a su presupuesto y objetivos.<br>

    ¡Vamos a hacer que su marca brille en todas partes!
    </p>
    <img data-aos-duration="1000" data-aos="zoom-in-right" class="photoTurism" src="/images/logoBlanco3.png" alt="" />
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
  .history-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;
    background-color: black;
    color: white;
    padding-top: 30px;
    padding-bottom: 30px;
  }

  .h1Title{
    padding-left: 20px;
  }

  .history-container img {
    width: 40%;
    grid-column: 2;
    grid-row: 2;
    margin: 0 auto;
    align-self: center;
  }

  .history-container .pSubtitle {
    grid-column: 1;
    grid-row: 2;
    padding: 20px;
    font-size: 20px;
  }
}


/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */

@media (max-width: 760px) {

  .history-container {
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
  }

  .photoTurism {
    width: 100%;
  }

}
</style>
  