<template>
  <div id="app">
    <Header
    @selectFilm="ricerca($event)"
    />
   <Main
   :arrayff="cards"

   />
    </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import axios from 'axios';

export default {
  name: "App",
   components: {
    Header,
    Main,
  },
  data() {
    return {
    query: "https://api.themoviedb.org/3/search/",
    api_key: "8698b0b53840a7e8db92ce738b54cc39",
    language: "en-US",
    filmSel: "",
    cards: [],
    }
  },
  methods: {
    setFilm(value) {
      this.filmSel = value;      
    },
    ricerca() {
       const endpoint = "movie";
      const parameters = {
        api_key: this.api_key,
        language: this.language,
        query2: this.filmSel,
      }
      axios.get(`${this.query}${endpoint}`, { params: parameters })
        .then((result) => {
            this.cards = result.data.results;      
        })
        .catch((error) => {
            console.log(error);
        })
    },
  }
};
</script>

<style lang="scss">

</style>
