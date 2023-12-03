<template>
  <div class="header-container">
    <video src="../../public/video/videoHeader.mp4" autoplay loop muted></video>
    <img
      src="../../public/images/logo.png"
      alt="Imagen"
      style="
        position: absolute;
        top: 60%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100px;
      "
    />
    <h1 class="nameH1">MATIAS <span style="color: #0523f6">BECHER</span></h1>

    <h1
      style="
        font-weight: 900;
        position: absolute;
        top: 90%;
        left: 50%;
        transform: translate(-50%, -50%);
      "
    >
    <i id="btnDown" class="bi bi-arrow-down-circle-fill"></i>
    </h1>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap");

* {
  font-family: "Oswald", sans-serif;
}

video {
  width: 100%;
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

#btnDown{
  color: #0523f6;
  font-size: 40px;
}

</style>
