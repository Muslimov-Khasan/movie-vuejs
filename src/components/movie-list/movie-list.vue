<template>
  <ul class="movie__list">
    <MovieItem v-for="movie in movies" v-bind:movie="movie" :class="[{like: movie.like}, {favourite: movie.favourite}]" />
  
  </ul>
</template>
<script>
import MovieItem from "../movie-list-item/movie-list-item.vue"
export default {
    components: { MovieItem },
    data() {
    return {
      movies: [
        {
          name: "Hulk",
          viewers: 118,
          favourite: false,
          like: true
        },
        {
          name: "Omar",
          viewers: 222,
          favourite: false,
          like: false
        },
        {
          name: "Iron",
          viewers: 123,
          favourite: true,
          like: false
        },
      ],
    };
  },
    
};
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
