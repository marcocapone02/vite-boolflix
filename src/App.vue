<script>
import axios, { Axios } from 'axios';
import { store } from './store';
import Search from './components/Search.vue';
import FindFilm from './components/FindFilm.vue';

export default {
  name: 'App',
  components:{
    Search,
    FindFilm
  },
  data() {
    return {
      store  
    }
  },
  methods: {
    SearchApi(){
      axios.all([
        axios.get(`https://api.themoviedb.org/3/search/movie?api_key=f65ad0c55ac9547d453d5b83f9f3f576&language=it_IT&query=${store.FilmName}`),
        axios.get(`https://api.themoviedb.org/3/search/tv?api_key=f65ad0c55ac9547d453d5b83f9f3f576&language=it_IT&query=${store.FilmName}`)
      ])
      .then(axios.spread((res1, res2) =>{
        const films_found = res1.data.results;
        const tv_found = res2.data.results;
        
        store.arrayFindFilm = films_found;
        store.arrayFoundTv = tv_found;
      }))
    }
  }
}
</script>

<template>
  <div id="boolflix" class="overflow-auto">
    <Search @searchFilm="SearchApi()"/>
    <FindFilm/>
  </div>
</template>

<style>
  #boolflix{
    height: 100vh;
    background-color: black;
  }
</style>