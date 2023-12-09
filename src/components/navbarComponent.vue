<template>
  <div class="navbar-container">
    <nav class="navbar sticky-top navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img class="logoImg" src="/images/logoBlanco3.png" />
        </a>
      
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link" @click="scroolToMatias" aria-current="page" href="#">MATIAS BECHER</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" @click="scroolToKarting" href="#">KARTING</a>
            </li>

            <li class="nav-item">
              <a class="nav-link" @click="scroolToTurismo">TURISMO PISTA</a>
            </li>

            
            <li class="nav-item">
              <a class="nav-link" @click="scroolToHistory">MI HISTORIA</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  methods: {
    scroolToMatias() {
      const height = document.getElementById("my-template").clientHeight
      window.scrollTo(0, height+100);
    },
    scroolToKarting(){
      const height = document.getElementById("my-template").clientHeight
      window.scrollTo(0,height+950)
    },
    scroolToTurismo(){
      const height = document.getElementById("my-template").clientHeight
      window.scrollTo(0,height+1550)
    },
    scroolToHistory(){
      const height = document.getElementById("my-template").clientHeight
      window.scrollTo(0,height+2200)
    },
    
  },
};
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');

* {
  font-family: 'Oswald', sans-serif;
}



.logoImg{
  filter: brightness(95%);
}

nav {
  background-color: #0b1fba !important;
  height: 15vh;
  z-index: 1;
}

nav .nav-link{
  font-weight: 900;
  font-size: 23px;
  color: white ;
}

.navbar img {
  width: 80px;
}

.navbar-toggler {
  background-color: #0b1fba ;
  border: none;
}

.navbar-toggler-icon {
  background-color: #0b1fba ;
  border-radius: 5px;
  
}
</style>
