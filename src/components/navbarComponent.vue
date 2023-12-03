<template>
  <div class="navbar-container">
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img class="logoImg" src="../../public/images/logo.png" />
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
              <a class="nav-link" aria-current="page" href="#">MATIAS BECHER</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">KARTING</a>
            </li>

            <li class="nav-item">
              <a class="nav-link">TURISMO PISTA</a>
            </li>

            
            <li class="nav-item">
              <a class="nav-link">MI HISTORIA</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
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
