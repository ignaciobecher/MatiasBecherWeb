<template>
    <navbarComponent></navbarComponent>
    <headerComponent></headerComponent>
    <aboutComponent></aboutComponent>
</template>

<script>
import navbarComponent from '../components/navbarComponent.vue';
import headerComponent from '../components/headerComponent.vue';
import aboutComponent from '../components/aboutComponent.vue';
export default {
    components:{
        navbarComponent,
        headerComponent,
        aboutComponent
    }
}
</script>