<template>
  <header>
      <ul>
          <li  v-for="(film, index) in arrayff"
          :key="index">
          <div v-if="(arrayff.length == 0)">
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
export default {
name: "Main",
data() {
    return {
    
    }
},
 computed: {
    
  },
    props: {
   testo: String,
   arrayff: Array,
  },
mounted() {
    
},
created() {
//  axios.get(`${this.query}${this.nameFilm}${this.query2}`)
//     .then((result) => {
//         console.log(result.data);
//         this.arrayFilm = result.data.results,
//         console.log("array", this.arrayFilm);
//         this.nameFilm = this.testo;
//         console.log("nome", this.namefilm);
//         // this.$emit('ricerca', this.nameFilm);
        
//     })
//     .catch((error) => {
//         console.log(error);
//     })
    
},
methods: {
// richiamo() {
//     axios.get(`${this.query}${this.testo}${this.query2}`)
//         .then((result) => {
//             this.arrayFilm = result.data.results, 
//             this.nameFilm = this.testo;           
//         })
//         .catch((error) => {
//             console.log(error);
//         })
// //  this.$emit('ricerca', this.nameFilm);
// // console.log(this.$emit);
// // console.log(this);
// }
}
}
</script>

<style>

</style>