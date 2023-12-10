<template>
    <div class="about-container">
       
        <p class="pSubtitle">
            <h1 class="h1Title">Matias Becher</h1>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur, voluptatem. Earum,
            laboriosam possimus rerum nisi ducimus doloremque illo voluptatum laborum eveniet temporibus quis consequatur
            vel, ipsa natus ex. Eveniet cum ut eaque soluta cupiditate harum esse? Repellendus nesciunt aliquam quaerat
            expedita impedit, cum optio labore quo totam odit accusamus! Error ipsum doloremque possimus alias doloribus
            maiores. Iure officiis vero fugiat? Ipsum cupiditate quidem soluta maiores quaerat asperiores eius similique eos
            rem sequi quod, placeat dolores cum eligendi aspernatur doloribus? Nesciunt?Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur, voluptatem. Earum,
            laboriosam possimus rerum nisi ducimus doloremque illo voluptatum laborum eveniet temporibus quis consequatur
            vel, ipsa natus ex. Eveniet cum ut eaque soluta cupiditate harum esse? Repellendus nesciunt aliquam quaerat
            expedita impedit, cum optio labore quo totam odit accusamus! Error ipsum doloremque possimus alias doloribus
            maiores. Iure officiis vero fugiat? Ipsum cupiditate quidem soluta maiores quaerat asperiores eius similique eos
            rem sequi quod, placeat dolores cum eligendi aspernatur doloribus? Nesciunt?</p>
        <img src="/images/fotoAbout.jpg" alt="" class="photoAbout">

    </div>
</template>

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
