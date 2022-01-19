<template>
  <div>Header</div>
</template>

<script>
import axios from 'axios';
export default {
name: "Main",
data() {
    return {
    nameFilm: "Ritorno"
    }
},
mounted() {
    axios.get(`https://api.themoviedb.org/3/search/movie?api_key=8698b0b53840a7e8db92ce738b54cc39&language=en-US&query=${this.nameFilm}&page=1&include_adult=false`)
    .then((result) => {
        console.log(result.data);
        

    })
    .catch((error) => {
        console.log(error);
    })
},
}
</script>

<style>

</style>