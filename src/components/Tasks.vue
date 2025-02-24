<template>
  <div class="button-container">
    <button class="styled-button" @click="$emit('show', 'Hello', 'World')">
      Нажми меня
    </button>
  </div>
</template>

<script setup>
</script>

<style scoped>
.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 300px; 
  width: 300px;
  background-color:rgb(255, 186, 219); 
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Легкая тень */
}

.styled-button {
  background-color:rgb(250, 62, 156); /* Розовая кнопка */
  color: white;
  border: none;
  border-radius: 10px;
  padding: 15px 30px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s; /* Плавный переход цвета фона и эффекта нажатия */
}

.styled-button:hover {
  background-color:rgb(193, 0, 100); /* Темно-розовый при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}
</style>