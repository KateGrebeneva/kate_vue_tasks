<template>
  <div class="container">
    <!-- Задание 1: Выводим значение свойства text в абзаце -->
    <p class="text-display">{{ text }}</p>
    
    <!-- Задание 3: Две кнопки для изменения текста на разные значения -->
    <div class="button-container">
      <button class="change-button" @click="changeToFirst">Изменить на 'flora'</button>
      <button class="change-button" @click="changeToSecond">Изменить на 'stella'</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'bloom', // Изначальное значение свойства text
    };
  },
  methods: {
    // Задание 3: Метод для изменения текста на 'flora'
    changeToFirst() {
      this.text = 'flora'; 
    },
    // Задание 3: Метод для изменения текста на 'stella'
    changeToSecond() {
      this.text = 'stella'; 
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
  background-color:rgb(238, 141, 198); /* Светлый фон для контраста */
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.text-display {
  font-size: 2em;
  color: #d5006d; /* Темно-розовый цвет текста */
  margin-bottom: 20px;
}

.button-container {
  display: flex;
  justify-content: center;
  gap: 10px; /* Отступ между кнопками */
}

.change-button {
  padding: 15px 25px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color: #d5006d; /* Темно-розовый цвет кнопок */
  color: white;
  font-size: 1em;
  transition: background-color 0.3s, transform 0.2s; /* Плавный переход */
}

.change-button:hover {
  background-color: #c51162; /* Более темный оттенок при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}
</style>