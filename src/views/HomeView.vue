<template>
  <div v-show="loaded">
    <navbarComponent></navbarComponent>
    <headerComponent></headerComponent>
    <aboutComponent></aboutComponent>
    <kartingComponent></kartingComponent>
    <turismoComponent></turismoComponent>
    <historyComponent></historyComponent>
    <footerComponent></footerComponent>
  </div>

  <div v-show="isLoading" class="heartbeat">
    <div class="heartbeat-container">
      <div class="heartbeat-inner">
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
      </div>
    </div>
  </div>
</template>

<script>
import navbarComponent from "../components/navbarComponent.vue";
import headerComponent from "../components/headerComponent.vue";
import aboutComponent from "../components/aboutComponent.vue";
import kartingComponent from "../components/kartingComponent.vue";
import turismoComponent from "../components/turismoComponent.vue";
import historyComponent from "../components/historyComponent.vue";
import footerComponent from "../components/footerComponent.vue";
export default {
  components: {
    navbarComponent,
    headerComponent,
    aboutComponent,
    kartingComponent,
    turismoComponent,
    historyComponent,
    footerComponent,
  },
  data() {
    return {
      isLoading: false,
      loaded: false,
    };
  },
  methods: {
    loadPage() {
      this.isLoading = true;
      this.loaded = false;
      setTimeout(() => {
        this.isLoading = false;
        this.loaded = true;
      }, 8000);
    },
  },
  mounted() {
    this.loadPage();
  },
};
</script>

<style scoped>

.heartbeat {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 10;
} 
.heartbeat-container {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100px;
  height: 100px;
}

.heartbeat-inner {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
 
  border-radius: 50%;
  background-color: #fff;
  animation: heartbeat 2s infinite linear;
}

@keyframes heartbeat {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
</style>
