<template>
  <header>
      <div class="title">
          <h2> Boolflix</h2>

          </div>
      <div class="search">
          <input v-model="nameFilm" type="text">
          <button @click="$emit('selectFilm', nameFilm)">Cerca</button>
      </div>
  </header>
</template>

<script>
export default {
name: "Header",
data() {
    return {
        nameFilm:"",
    }
},
methods: {

},
}
</script>

<style lang="scss">
header {
    background-color: black;
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    .title {
        color: red;
        h2 {
            font-size: 2.3em;
            text-transform: uppercase;
        }
    }
    .search{
        button {
            margin-left: 30px;
            width: 60px;
            height: 25px;
            border: 2px solid red;
            background-color: black;
            color: red;
            border-radius: 15px;
            text-transform: uppercase;
        }
        input {
            height: 25px;
            width: 200px;
            border: none;
            border-radius: 15px;
        }

    } 
}
</style>>

