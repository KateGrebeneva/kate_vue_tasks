<template>
  <div class="user-container">
    <button class="action-button" @click="handleAnimation">Воспроизвести анимацию</button>
    <button class="action-button" @click="handleCartoon">Воспроизвести мультик</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue'

const emit = defineEmits(['show-animation', 'show-cartoon'])

const handleAnimation = () => {
  emit('show-animation')
}

const handleCartoon = () => {
  emit('show-cartoon')
}
</script>

<style scoped>
.user-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color:rgb(247, 183, 209); /* Светлый фон для дочернего компонента */
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Легкая тень */
}

.action-button {
  background-color:rgb(255, 74, 165); /* Розовая кнопка */
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  margin: 10px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s; /* Плавный переход цвета фона и эффекта нажатия */
}

.action-button:hover {
  background-color:rgb(185, 0, 96); /* Темно-розовый при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}
</style>