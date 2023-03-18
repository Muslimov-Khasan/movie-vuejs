<template>
  <div class="container font-monospace">
    <div class="content">
      <AppInfo
        :allMovieContent="movies.length"
        :favouriteMoviesCoount="movies.filter((c) => c.favourite).length"
      />
      <div class="search__panel">
        <SearchPanle />
        <FilterPanle />
      </div>
      <MovieList
        :movies="movies"
        @onLike="onLikeHandle"
        @onToggle="onToggleHandle"
      />
      <MovieAddForm @createMovie="createMovie" />
    </div>
  </div>
</template>

<style>
.container {
  height: 100vh;
}

.content {
  width: 1000px;
  min-height: 700px;
  margin: 0 auto;
  padding: 5rem 0;
}

.search__panel {
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 4px;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  background-color: #fcfaf5;
}
</style>

<script>
import AppInfo from "./../movie-info/movie-info.vue";
import SearchPanle from "./../search-panle/search-panle.vue";
import FilterPanle from "./../app-filter/app-filter.vue";
import MovieList from "./../movie-list/movie-list.vue";
import MovieAddForm from "./../Movie-add-form/Movie-add-form.vue";
export default {
  components: {
    AppInfo,
    SearchPanle,
    FilterPanle,
    MovieList,
    MovieAddForm,
  },
  data() {
    return {
      movies: [
        {
          id: 1,
          name: "Hulk",
          viewers: 118,
          favourite: false,
          like: false,
        },
        {
          id: 2,
          name: "Omar",
          viewers: 222,
          favourite: false,
          like: false,
        },
        {
          id: 3,
          name: "Iron",
          viewers: 123,
          favourite: true,
          like: true,
        },
      ],
    };
  },
  methods: {
    createMovie(item) {
      this.movies.push(item);
    },
    onToggleHandle(id, prop) {
      this.movies = this.movies.map((item) => {
        if (item.id === id) {
          return {...item, [prop]: !item[prop]}
        }
        return item;
      });
    },
   
  },
};
</script>
