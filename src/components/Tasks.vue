<template>
  <div class="container">
    <!-- Задание 1: Выводим значение свойства text в абзаце -->
    <p class="text-display">{{ text }}</p>
    
    <!-- Задание 2: Кнопка для изменения текста -->
    <button class="change-button" @click="change">Изменить текст</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Изначальное значение свойства text
      text: 'xxx', 
    };
  },
  methods: {
    // Задание 2: Метод для изменения текста на 'yyy'
    change() {
      this.text = 'yyy'; // Изменяем текст на 'yyy'
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
  background-color:rgb(245, 150, 205); 
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.text-display {
  font-size: 2em;
  color: #d5006d;
  margin-bottom: 20px;
}

.change-button {
  padding: 15px 25px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color: #d5006d; 
  color: white;
  font-size: 1em;
  transition: background-color 0.3s, transform 0.2s; 
}

.change-button:hover {
  background-color: #c51162; 
  transform: scale(1.05); 
}
</style>