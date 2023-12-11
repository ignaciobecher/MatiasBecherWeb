<template>
    <h1 class="h1Title">Galeria de imagenes</h1>

    <div class="images-container">
        <div class="images">
            <img loading="eager" src="/images/Kart.jpg" alt="" />
        </div>
        <div class="images">
            <img loading="eager" src="/images/turismo6.jpeg" alt="" />
        </div>
      
        <div class="images">
            <img loading="eager" src="/images/history.jpg" alt="" />
        </div>
        <div class="images">
            <img loading="eager" src="/images/karting3.jpeg" alt="" />
        </div>
        <div class="images">
            <img loading="eager" src="/images/karting1.jpeg" alt="" />
        </div>
        <div class="images">
            <img loading="eager" src="/images/kartin2.jpeg" alt="" />
        </div>
        
        <div class="images">
            <img loading="eager" src="/images/Kart.jpg" alt="" />
        </div>
        <div class="images">
            <img loading="eager" src="/images/turismo5.jpeg" alt="" />
        </div>
    </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500&display=swap");

* {
    font-family: "Oswald", sans-serif;
}

/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES------------------------ */

@media (min-width: 761px) {
    .h1Title {
        text-align: center;
        background-color: #0b1fba !important;
        margin: 0;
        color: white;
    }

    .images-container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-rows: auto auto auto;
        background-color: #0b1fba !important;
    }

  

    .images img {
        width: 100%;
        padding: 2px;
        border-radius: 15px;
    }
}

/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */

@media (max-width: 760px) {
    .h1Title {
        text-align: center;
        background-color: #0b1fba !important;
        margin: 0;
        color: white;
        padding-bottom: 30px;
        padding-top: 30px;
    }
    
    .images-container{
        background-color: #0b1fba !important;
    }

    .images img{
        width: 100%;
        border-radius: 15px;
        padding: 10px;
    }
}
</style>
