<template>
  <div class="employee-card">
    <h2 class="employee-name">{{ name }}</h2>
    <p class="employee-info">Зарплата: {{ salary }}$</p>
    <p class="employee-info">Возраст: {{ age }} лет</p>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

// Определяем типы пропсов
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  salary: {
    type: Number,
    required: true
  },
  age: {
    type: Number,
    required: true
  }
})
</script>

<style scoped>
.employee-card {
  background-color:rgb(248, 193, 219); /* Светло-розовый фон для карточки работника */
  border: 2px solid rgb(213, 27, 120); /* Розовая граница */
  border-radius: 10px;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Легкая тень для карточки */
}

.employee-name {
  color:rgb(164, 0, 85); /* Темно-розовый цвет имени */
  font-size: 1.5rem; /* Увеличенный размер шрифта для имени */
}

.employee-info {
  color: #333; /* Цвет текста для информации */
  font-size: 1rem; /* Размер шрифта для информации */
  color:rgb(188, 0, 97);
}
</style>