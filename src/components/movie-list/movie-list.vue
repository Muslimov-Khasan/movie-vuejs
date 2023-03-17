<template>
  <ul class="movie__list">
    <MovieItem v-for="movie in movies" v-bind:movie="movie" :class="[{like: movie.like}, {favourite: movie.favourite}]" />
  
  </ul>
</template>
<script>
import MovieItem from "../movie-list-item/movie-list-item.vue"
export default {
    components: { MovieItem },
   props: {
    movies: {
      type: Array,
      requeired: true,
    }
   } 
}
</script>
<style scoped>
.movie__list {
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 4px;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  background-color: #fcfaf5;
}
</style>
