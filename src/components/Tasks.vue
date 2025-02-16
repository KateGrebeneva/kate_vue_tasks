<template>
  <div class="container">
    <!-- Задание 1: Выводим цену, количество и полную стоимость -->
    <h2 class="title">Информация о продукте</h2>
    <p class="info">Цена продукта: <span class="highlight">{{ cost }}₽</span></p>
    <p class="info">Количество: <span class="highlight">{{ amount }}</span></p>
    <p class="info">Полная стоимость: <span class="highlight">{{ price }}₽</span></p>

    <!-- Задание 2: Кнопка для изменения количества -->
    <button class="change-button" @click="increaseAmount">Увеличить количество</button>
    <button class="change-button" @click="decreaseAmount">Уменьшить количество</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Изначальные значения для цены и количества
      cost: 100, // Цена продукта
      amount: 1, // Количество продукта
    };
  },
  computed: {
    // Вычисляемое свойство для полной стоимости
    price() {
      return this.cost * this.amount; // Полная стоимость = цена * количество
    },
  },
  methods: {
    // Метод для увеличения количества
    increaseAmount() {
      this.amount += 1; // Увеличиваем количество на 1
    },
    // Метод для уменьшения количества
    decreaseAmount() {
      if (this.amount > 1) {
        this.amount -= 1; // Уменьшаем количество на 1, если оно больше 1
      }
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
  background-color:rgb(248, 165, 213); 
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  font-size: 2em;
  color: #d5006d; 
}

.info {
  font-size: 1.5em;
  color: #d5006d; 
}

.highlight {
  font-weight: bold;
}

.change-button {
  padding: 15px 25px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color:rgb(208, 47, 130); 
  color: white;
  font-size: 1em;
  margin: 10px;
  transition: background-color 0.3s, transform 0.2s; 
}

.change-button:hover {
  background-color: #c51162; 
  transform: scale(1.05); 
}
</style>