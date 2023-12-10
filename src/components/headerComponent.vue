<template>
  <div id="my-template" class="header-container">
    <video autoplay loop muted playsinline>
      <source src="../assets/videoComp.mp4" type="video/mp4" preload="auto" lazyload />
    </video>
    <img
      src="/images/logoFirma.png"
      alt="Imagen"
      style="
        position: absolute;
        top: 90%;
        left: 80%;
        transform: translate(-50%, -50%);
        width: 100px;
      "
    />

    <h1
      style="
        font-weight: 900;
        position: absolute;
        top: 90%;
        left: 50%;
        transform: translate(-50%, -50%);
      "
    >
      <i
        id="btnDown"
        @click="scrollToBottom"
        class="bi bi-arrow-down-circle-fill"
      ></i>
    </h1>
  </div>

  <div class="header-monitor-container">
    <div class="images">
      <img loading="eager" src="/images/fotoAbout.jpg" alt="">
    </div>
    <div class="images">
      <img loading="eager" src="/images/headerMain.jpg" alt="">
    </div>
    <div class="images">
      <img loading="eager" src="/images/turismo2.jpg" alt="">
    </div>
    <div class="images">
      <img loading="eager" src="/images/headerMain2.jpg" alt="">
    </div>
  </div>
</template>

<script>
import VueLazyload from "vue-lazyload";
export default {
  components: { VueLazyload },
  data() {
    return {
      isLoading: false,
    };
  },
  methods: {
    scrollToBottom() {
      const height = document.getElementById("my-template").clientHeight;
      window.scrollTo(0, height + 100);
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap");

* {
  font-family: "Oswald", sans-serif;
}

/*-------------------------------- RESPONSIVE PARA PANTALLAS GRANDES----------------------------- */

@media (min-width: 761px) {
  .header-container {
    display: none;
  }

  .header-monitor-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: auto;
  }

  .images img {
    width: 100%;
    height: 100%;
    filter: grayscale(1);
    transition: filter 500ms ease-in-out;
  }



  .images img:hover {
    filter: none;
  }

}

/*-------------------------------- RESPONSIVE PARA DISPOSITIVOS PEQUEÑOS------------------------ */
@media (max-width: 760px) {
  .header-monitor-container{
    display: none;
  }

.header-container {
  background-color: #0b1fba;
}

  video {
    width: 100%;
    filter: brightness(60%);
  }

  .nameH1 {
    color: black;
    font-weight: 900;
    position: absolute;
    top: 70%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
    text-align: center;
  }

#btnDown {
  color: #0523f6;
  font-size: 40px;
}
</style>
