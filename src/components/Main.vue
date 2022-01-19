<template>
  <header>
      <ul>
          <li  v-for="(film, index) in arrayFilm"
          :key="index">
          <div v-if="(arrayFilm.length == 0)">
              vuoto
          </div>
          <div v-else>
          Titolo:{{film.title}}
          Titolo Originale {{film.original_title}}
          Lingua {{film.original_language}}
          Voto {{film.vote_average}}

          </div>
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
    nameFilm: "",
    arrayFilm: [],
    query: "https://api.themoviedb.org/3/search/movie?api_key=8698b0b53840a7e8db92ce738b54cc39&language=en-US&query=",
    query2: "&page=1&include_adult=false"
    }
},
 computed: {
    
  },
    props: {
   testo: String,
  },
mounted() {
    
},
created() {
 axios.get(`${this.query}${this.nameFilm}${this.query2}`)
    .then((result) => {
        console.log(result.data);
        this.arrayFilm = result.data.results,
        console.log("array", this.arrayFilm);
        this.nameFilm = this.testo;
        console.log("nome", this.namefilm);
    })
    .catch((error) => {
        console.log(error);
    })
    
}
}
</script>

<style>

</style>