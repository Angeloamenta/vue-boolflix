<template>
  <header>
      <ul>
          <li v-for="(film, index) in arrayFilm"
          :key="index">
          {{film.title}}
          </li>
      </ul>
  </header>
</template>

<script>
import axios from 'axios';
export default {
name: "Main",
data() {
    return {
    nameFilm: "Ritorno",
    arrayFilm: [],
    }
},
mounted() {
    axios.get(`https://api.themoviedb.org/3/search/movie?api_key=8698b0b53840a7e8db92ce738b54cc39&language=en-US&query=${this.nameFilm}&page=1&include_adult=false`)
    .then((result) => {
        console.log(result.data);
        this.arrayFilm = result.data.results,
        console.log("array", this.arrayFilm);
    })
    .catch((error) => {
        console.log(error);
    })
},
}
</script>

<style>

</style>