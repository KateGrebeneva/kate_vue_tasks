<template>
  <div class="positive-numbers-container">
    <h1 class="title">Положительные числа</h1>
    <ul>
      <template v-for="item in items">
        <li v-if="item > 0" :key="item" class="number-item">
          {{ item }}
        </li>
      </template>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PositiveNumbers',
  data() {
    return {
      items: [1, -2, 3, -4, 5],
    };
  },
};
</script>

<style scoped>
.positive-numbers-container {
  background-color:rgb(249, 200, 228); /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  color: #d5006d; /* Темно-розовый заголовок */
  text-align: center;
  font-family: 'Arial', sans-serif; /* Шрифт заголовка */
  margin-bottom: 20px;
}

.number-item {
  color: #d5006d; /* Темно-розовая текст */
  font-size: 18px; /* Размер шрифта для чисел */
  margin: 5px 0; /* Отступы между элементами списка */
  padding: 10px; /* Отступ внутри элемента списка */
  border: 2px solid #d5006d; /* Темно-розовая рамка */
  border-radius: 10px; /* Закругление углов рамки */
  transition: background-color 0.3s, transform 0.2s; /* Анимация при наведении */
}

.number-item:hover {
  background-color: #f1c4d4; /* Светло-розовый фон при наведении */
  transform: scale(1.05); /* Увеличение при наведении */
}
</style>