<template>
  <div id="my-template" class="header-container">
    <video autoplay loop muted playsinline>
      <source src="/video/videoheader2.mp4" type="video/mp4" />
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

 
</template>

<script>
export default {
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
