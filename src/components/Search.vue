<script>
import { store } from "../store";
export default {
    name: 'Search',
    data() {
        return {
            store            
        }
    },
}
</script>

<template>
    <div class="input-group mt-4 mb-4 w-25 m-auto">
        <input type="text" class="form-control" placeholder="Cerca su BoolFlix" v-model="store.FilmName">
        <button class="btn btn-danger" type="button" @click="$emit('searchFilm')">Cerca</button>
    </div>
</template>

<style scoped>
</style>