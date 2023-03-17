<template>
  <div>
    <div class="movie__add-from">
      <h2>Yangi kino qo'shish</h2>
      <form class="form-add d-flex">
        <input
          class="form-control new__movie-lable"
          type="text"
          placeholder="qanday kino?!"
        />
        <input
          class="form-control new__movie-lable"
          type="number"
          placeholder="Nechi marotaba ko'rilgan?!"
        />
        <button class="btn btn-outline-dark">Qo'shish</button>
      </form>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.movie__add-from {
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 4px;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  background-color: #fcfaf5;
}
</style>
