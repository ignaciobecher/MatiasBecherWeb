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
              <a
                class="nav-link underline"
                @click="scroolToMatias"
                aria-current="page"
                href="#"
                >MATIAS BECHER</a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link underline" @click="scroolToKarting" href="#"
                >KARTING</a
              >
            </li>

            <li class="nav-item">
              <a class="nav-link underline" @click="scroolToTurismo" href="#"
                >TURISMO PISTA</a
              >
            </li>

            <li class="nav-item">
              <a class="nav-link underline" @click="scroolToHistory" href="#"
                >MI HISTORIA</a
              >
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
      const height = document.getElementById("my-template").clientHeight;
      if (window.innerWidth > 765) {
        window.scrollTo(0, height + 600);
      } else {
        window.scrollTo(0, height + 100);
      }
    },
    scroolToKarting() {
      const height = document.getElementById("my-template").clientHeight;
      if (window.innerWidth > 765) {
        window.scrollTo(0, height + 1600);
      } else {
        window.scrollTo(0, height + 950);
      }
    },
    scroolToTurismo() {
      const height = document.getElementById("my-template").clientHeight;
      if (window.innerWidth > 765) {
        window.scrollTo(0, height + 2100);
      } else {
        window.scrollTo(0, height + 1550);
      }
    },
    scroolToHistory() {
      const height = document.getElementById("my-template").clientHeight;
      if (window.innerWidth > 765) {
        window.scrollTo(0, height + 2800);
      } else {
        window.scrollTo(0, height + 2200);
      }
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap");

* {
  font-family: "Oswald", sans-serif;
}

@media (min-width: 761px) {
  .logoImg {
    filter: brightness(95%);
  }

  nav {
    background-color: #0b1fba !important;
    height: 15vh;
    z-index: 1;
  }

  nav .nav-link {
    font-weight: 900;
    font-size: 23px;
    color: white;
  }

  .navbar img {
    width: 80px;
  }

  .navbar-toggler {
    background-color: #0b1fba;
    border: none;
  }

  .navbar-toggler-icon {
    background-color: #0b1fba;
    border-radius: 5px;
  }
  .underline {
    position: relative;
  }

  .underline::before {
    content: "";
    position: absolute;
    bottom: 0;
    right: 0;
    width: 0;
    height: 2px;
    background-color: white;
    transition: width 0.6s cubic-bezier(0.25, 1, 0.5, 1);
  }

  @media (hover: hover) and (pointer: fine) {
    .underline:hover::before {
      left: 0;
      right: auto;
      width: 100%;
    }
  }
}

@media (max-width: 760px) {
  .logoImg {
    filter: brightness(95%);
  }

  nav {
    background-color: #0b1fba !important;
    height: 15vh;
    z-index: 1;
  }

  nav .nav-link {
    font-weight: 900;
    font-size: 23px;
    color: white;
  }

  .navbar img {
    width: 80px;
  }

  .navbar-toggler {
    background-color: #0b1fba;
    border: none;
  }

  .navbar-toggler-icon {
    background-color: #0b1fba;
    border-radius: 5px;
  }
}
</style>
