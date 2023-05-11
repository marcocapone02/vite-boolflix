<script>
export default {
    name: 'CardFilm',
    props: ['detailsFilm'],
}
</script>

<template>
    <div class="card col-3">
        <img :src="'https://image.tmdb.org/t/p/original' + detailsFilm.poster_path" class="card-img-top" :alt="detailsFilm.title">
        <div class="card-body">
            <h5 class="card-title">{{ detailsFilm.title }}</h5>
            <p class="card-text">{{ detailsFilm.overview }}</p>

            <div class="stars">
                <span class="fa fa-star"></span>
                <span class="fa fa-star"></span>
                <span class="fa fa-star"></span>
                <span class="fa fa-star"></span>
                <span class="fa fa-star"></span>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .checked{
        color: yellow;
    }
</style>