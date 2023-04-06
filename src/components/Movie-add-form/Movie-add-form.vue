<template>
  <div>
    <div class="movie__add-from">
      <h2>Yangi kino qo'shish</h2>
      <form class="form-add d-flex" @submit.prevent>
        <input
          class="form-control new__movie-lable"
          type="text"
          placeholder="qanday kino?!"
          :value="name"
          @input="name = $event.target.value"
        />
        <input
          class="form-control new__movie-lable"
          type="number"
          placeholder="Nechi marotaba ko'rilgan?!"
          @input="viewers = $event.target.value"
        />
        <button class="btn btn-outline-dark" @click="addMovie">Qo'shish</button>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      viewers: "",
    }
  },
  methods: {
    addMovie() {
     if (!this.name || !this.viewers) return;
    const newMovie = {
     id: Date.now(),
     name: this.name,
     viewers: this.viewers,
     favourite: false,
     like: false,
    }
    this.$emit("createMovie", newMovie)
    this.name = ""
    this.viewers = ""
   }
  }
};
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
