<template>
  <div class="app-info">
    <p class="fs-3 text-uppercaese">
      Barcha kinolar soni: {{ allMovieContent }}
    </p>
    <p class="fs-4 text-uppercaese">ko'rilgan kinolar ksoni: {{ favouriteMoviesCoount }}</p>
  </div>
</template>

<script>
export default {
  props: {
    allMovieContent: {
      type: Number,
      required: true,
    },
    favouriteMoviesCoount: {
      type: Number,
      required: true,
    }
  },
 
};
</script>

<style scoped>
.app-info {
  padding: 27px;
  border-radius: 5px;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  background-color: #fcfaf5;
}
</style>
