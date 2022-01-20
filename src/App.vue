<template>
  <div id="app">
    <Header
    @selectFilm="setFilm($event)"
    />
   <Main
   :arrayff="cards"
   :arraySeries="tvSeries"
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
    tvSeries: [],
    };
  },
  methods: {
    setFilm(value) {
       this.filmSel = value;    
      console.log(this.filmSel);  
      this.ricerca();
      this.ricercaDue();
    },
    search(value) {
      this.filmSel = value; 
      this.ricerca();
    },
    ricerca() {
       const endpoint = "movie";
      const parameters = {
        api_key: this.api_key,
        language: this.language,
        query: this.filmSel,
      };
      axios.get(`${this.query}${endpoint}`, { params: parameters }).then((result) => {
        this.cards = result.data.results;  
        console.log("film", this.cards);    
        })
        .catch((error) => {
            console.log(error);
        })
    },
    ricercaDue() {
       const endpoint = "tv";
      const parameters = {
        api_key: this.api_key,
        language: this.language,
        query: this.filmSel,
      };
      axios.get(`${this.query}${endpoint}`, { params: parameters }).then((result) => {
        this.tvSeries = result.data.results; 
        console.log("serie", this.tvSeries);     
        })
        .catch((error) => {
            console.log(error);
        })
    },
  }
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss"
</style>
