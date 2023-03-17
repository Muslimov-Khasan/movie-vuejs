<template>
  <li class="list__group-item d-flex justify-content-between">
    <span class="list-group-label">{{ movie.name }}</span>
    <input class="list-group-item-input" type="number" v-bind:value="movie.viewers"/>
    <div class="d-flex justify-content-center align-items-center">
      <button class="btn-cookie btn-sm">
        <i class="fas fa-cookie"></i>
      </button>
      <button class="btn-trash btn-sm">
        <i class="fas fa-trash"></i>
      </button>
      <i class="fas fa-star"></i>
    </div>
  </li>
</template>
<script>
export default {
  props: {
    movie: {
        type: Object,
        required: true,
    }
  }
};
</script>
<style scoped>
.list__group-item {
  padding: 15px 20px;
  border: none;
  border-bottom: 1px solid #302e29;
}

.list__group-item:last-child {
  border-bottom: none;
}

.list__group-item span {
  line-height: 35px;
  font-size: 20px;
  cursor: pointer;
  width: 550px;
}

.list__group-item input {
  line-height: 35px;
  font-size: 20px;
  text-align: center;
  border: none;
  outline: none;
}

.list__group-item button {
  width: 40px;
  height: 40px;
  margin: 3px;
  font-size: 17px;
  border: none;
  cursor: pointer;
}

.list__group-item .btn-cookie {
  color: #e09f3e;
}
.list__group-item .btn-trash {
  color: rgb(199, 70, 41);
}
.list__group-item .fa-star {
  color: rgb(199, 70, 41);
  width: 40px;
  height: 40px;
  text-align: center;
  line-height: 35px;
  font-size: 17px;
  color: gold;
  transition: 0.3s all;
  transform: translate(30px);
  opacity: 0;
}

.list__group-item.like .fa-star {
  opacity: 1;
  transform: translateX(0);
}

.list__group-item.favourite .list-group-label {
  color: #e09f3e;
}
.list__group-item.favourite .list-group-item-input {
  color: #e09f3e;
}
</style>
