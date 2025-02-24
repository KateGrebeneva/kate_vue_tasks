<template>
  <div class="employee-container">
    <h2 class="employee-title">Работник</h2>
    <button class="send-button" @click="handleSendInfo">Отправить информацию о работнике</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue'

const emit = defineEmits(['send-info'])

const handleSendInfo = () => {
  const employeeName = 'David'; // Имя работника
  const employeeSalary = '50000'; // Зарплата работника
  emit('send-info', employeeName, employeeSalary);
}
</script>

<style scoped>
.employee-container {
  background-color:rgb(255, 205, 225); /* Светлый фон для дочернего компонента */
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Легкая тень */
}

.employee-title {
  color:rgb(182, 2, 95); /* Темно-розовый цвет заголовка */
  text-align: center;
}

.send-button {
  background-color:rgb(235, 36, 135); /* Розовая кнопка */
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  margin-top: 10px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s; /* Плавный переход цвета фона и эффекта нажатия */
}

.send-button:hover {
  background-color:rgb(171, 5, 91); /* Темно-розовый при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}
</style>