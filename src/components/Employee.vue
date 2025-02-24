<template>
  <div class="employee-card">
    <h2 class="employee-name">{{ name }}</h2>
    <p class="employee-info">Зарплата: {{ salary }}$</p>
    <p class="employee-info">Возраст: {{ age }} лет</p>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

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
  background-color:rgb(255, 207, 230); /* Светло-розовый фон для карточки работника */
  border: 2px solid rgb(199, 12, 105); /* Розовая граница */
  border-radius: 10px;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Легкая тень для карточки */
  transition: transform 0.3s; /* Плавный переход при наведении */
}

.employee-card:hover {
  transform: scale(1.05);
}

.employee-name {
  color: #d5006d; 
  font-size: 1.5rem; 
}

.employee-info {
  color: #333; 
  font-size: 1rem; 
  color: #d5006d;
}
</style>