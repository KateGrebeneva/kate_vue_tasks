<template>
  <div class="container">
    <h1 class="title">Квадрат числа</h1>
    <div class="button-container">
      <button @click="showSquare(2)" class="button">Квадрат 2</button>
      <button @click="showSquare(3)" class="button">Квадрат 3</button>
      <button @click="showSquare(4)" class="button">Квадрат 4</button>
      <button @click="showSquare(5)" class="button">Квадрат 5</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    // Метод, принимающий число и выводящий его квадрат
    showSquare(num) {
      const square = num * num;
      alert("Квадрат числа " + num + " равен " + square);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color:rgb(245, 162, 231); 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D; 
  font-family: 'Arial', sans-serif;
  font-size: 24px;
  margin-bottom: 20px;
}

.button-container {
  display: flex;
  justify-content: center;
  gap: 15px; 
}

.button {
  background-color:rgb(229, 72, 153); 
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s;
}

.button:hover {
  background-color: #a4004e; 
  transform: scale(1.05); 
}
</style>
