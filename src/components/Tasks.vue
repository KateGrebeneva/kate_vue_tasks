<template>
  <div class="container">
    <h1 class="title">Task#8: Сумма элементов объекта</h1>
    <p class="sum">Сумма: {{ totalSum }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: { x: 1, y: 2, z: 3 }, // Объект с элементами
    };
  },
  computed: {
    totalSum() {
      // Вычисляем сумму значений объекта
      return Object.values(this.obj).reduce((acc, curr) => acc + curr, 0);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color:rgb(248, 202, 236); /* Светлый фон для контраста */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D; /* Темно-розовый цвет заголовка */
  font-family: 'Arial', sans-serif;
  margin-bottom: 15px;
}

.sum {
  font-size: 1.5em;
  color: #D5006D; /* Темно-розовый цвет суммы */
}
</style>
