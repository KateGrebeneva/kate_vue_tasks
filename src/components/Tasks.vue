<template>
  <div class="task-3">
    <h2>Задание 3</h2>
    <input v-model.number="number" placeholder="Введите число">
    <p>Квадрат числа: {{ number * number }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
    };
  },
};
</script>

<style scoped>
.task-3 {
  background-color:rgb(255, 155, 205);
  padding: 20px;
  border-radius: 10px;
  color: white;
}
input {
  padding: 10px;
  border-radius: 5px;
  border: none;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
p, h2 {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
</style>