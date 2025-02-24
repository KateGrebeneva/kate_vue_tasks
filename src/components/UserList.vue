<template>
  <div class="user-list">
    <h1 class="list-title">Список работников</h1>
    <Employee
      v-for="user in users"
      :key="user.id"
      :name="user.name"
      :salary="user.salary"
      :age="user.age"
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Employee from './Employee.vue' // Импортируем компонент Employee

const users = ref([
  {
    id: 1,
    name: 'Cora',
    salary: 10000,
    age: 30,
  },
  {
    id: 2,
    name: 'Robbin',
    salary: 20500,
    age: 29,
  },
  {
    id: 3,
    name: 'Regina',
    salary: 31000,
    age: 25,
  },
])
</script>

<style scoped>
.user-list {
  background-color:rgb(255, 205, 225); /* Светлый фон для списка работников */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Легкая тень для списка */
}

.list-title {
  color: #d5006d; /* Цвет заголовка списка */
  text-align: center;
  margin-bottom: 20px;
}
</style>