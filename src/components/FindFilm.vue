<script>
import { store } from "../store";
import CardFilm from "./CardFilm.vue";
export default {
    name: 'FindFilm',
    components:{
        CardFilm
    },
    data() {
        return {
            store            
        }
    },
}
</script>

<template>
    <div class="container">
        <div class="row justify-content-center gap-4">
            <CardFilm v-for="(elem, index) in store.arrayFoundAll" :key="index" :detailsFilm="elem"/>
        </div>
    </div>
</template>

<style scoped>  
</style>