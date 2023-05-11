<script>
export default {
    name: 'CardTV',
    props: ['detailsTv']
}
</script>

<template>
    <div class="card col-3">
        <img :src="'https://image.tmdb.org/t/p/original' + detailsTv.poster_path" class="card-img-top" :alt="detailsTv.name">
        <div class="card-body">
            <h5 class="card-title">{{ detailsTv.name }}</h5>
            <p class="card-text">{{ detailsTv.overview }}</p>
        </div>
    </div>
</template>

<style scoped>
    
</style>