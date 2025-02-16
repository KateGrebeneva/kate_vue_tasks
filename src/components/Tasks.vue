<template>
  <div class="container">
    <h2 class="title">Task#7_1: Элементы массива</h2>
    <div class="array-items">
      <p v-for="(item, index) in arr1" :key="index" class="item">{{ item }}</p>
    </div>

    <h2 class="title">Task#7_2: Сумма элементов массива</h2>
    <p class="sum">Сумма: {{ sum }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr1: ['x', 'y', 'z'], // Массив для задания №1
      arr2: [1, 2, 3], // Массив для задания №2
    }
  },
  computed: {
    sum() {
      return this.arr2.reduce((acc, curr) => acc + curr, 0); // Вычисляем сумму элементов массива
    }
  }
}
</script>

<style scoped>
.container {
  text-align: center;
  background-color:rgba(255, 73, 188, 0.59); 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D; 
  font-family: 'Arial', sans-serif;
  margin-bottom: 15px;
}

.array-items {
  margin-bottom: 20px;
}

.item {
  color: #D5006D;
  font-size: 1.5em;
  margin: 10px 0;
}

.sum {
  font-size: 1.5em;
  color: #D5006D; 
}
</style>


