<script>
export default {
    name: 'CardFilm',
    props: ['detailsFilm']
}
</script>

<template>
    <div class="card col-2">
        <img :src="'https://image.tmdb.org/t/p/original' + detailsFilm.poster_path" class="card-img-top" alt="">
        <div class="card-body">
            <h5 class="card-title">{{ detailsFilm.original_title }}</h5>
            <p class="card-text">{{ detailsFilm.overview }}</p>
        </div>
    </div>
</template>

<style scoped> 
</style>