<template>
    <navbarComponent></navbarComponent>
    <headerComponent></headerComponent>
    <aboutComponent></aboutComponent>
    <kartingComponent></kartingComponent>
    <turismoComponent></turismoComponent>
    <historyComponent></historyComponent>
    <footerComponent></footerComponent>
</template>

<script>
import navbarComponent from '../components/navbarComponent.vue';
import headerComponent from '../components/headerComponent.vue';
import aboutComponent from '../components/aboutComponent.vue';
import kartingComponent from '../components/kartingComponent.vue';
import turismoComponent from '../components/turismoComponent.vue';
import historyComponent from '../components/historyComponent.vue';
import footerComponent from '../components/footerComponent.vue'
export default {
    components:{
        navbarComponent,
        headerComponent,
        aboutComponent,
        kartingComponent,
        turismoComponent,
        historyComponent,
        footerComponent
    }
}
</script>