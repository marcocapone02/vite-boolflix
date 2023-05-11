<script>
import { store } from "../store";
import CardFilm from "./CardFilm.vue";
import CardTV from "./CardTV.vue";

export default {
    name: 'FoundFilms',
    components:{
        CardFilm,
        CardTV
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container">

        <h2 v-if="store.arrayFindFilm != 0" class="text-light">Film:</h2>
        <div class="row justify-content-center gap-4">
            <CardFilm v-for="(elem, index) in store.arrayFindFilm" :key="'Film-' + index" :detailsFilm="elem"/>
        </div>
        
        <h2 v-if="store.arrayFindFilm != 0" class="text-light">Serie TV:</h2>
        <div class="row justify-content-center gap-4">
            <CardTV v-for="(elem, index) in store.arrayFoundTv" :key="'Tv-' + index" :detailsTv="elem"/>
        </div>

    </div>
</template>

<style scoped>
    
</style>