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
  name: String,
  salary: Number,
  age: Number,
})
</script>

<style scoped>
.employee-card {
  background-color:rgb(255, 181, 210); /* Светло-розовый фон для карточки работника */
  border: 2px solid rgb(230, 43, 136); /* Розовая граница */
  border-radius: 10px;
  padding: 15px;
  margin-bottom: 15px;
}

.employee-name {
  color: #d5006d; /* Темно-розовый цвет имени */
}

.employee-info {
  color: #333; /* Цвет текста для информации */
}
</style>