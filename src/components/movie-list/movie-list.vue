<template>
  <ul class="movie__list">
    <MovieItem/>
    <MovieItem/>
    <MovieItem/>
  </ul>
</template>
<script>
import MovieItem from "../movie-list-item/movie-list-item.vue"
export default {
    components: { MovieItem }
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
