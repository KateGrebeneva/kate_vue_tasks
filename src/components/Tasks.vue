<template>
  <div class="container">
    <h2>Работники</h2>
    
    <div class="task" id="remove-worker-task">
      <h3>Задание 2: Удаление работника</h3>
      <table class="worker-table">
        <thead>
          <tr>
            <th>ID</th>
            <th>Имя</th>
            <th>Зарплата</th>
            <th>Возраст</th>
            <th>Действия</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="user in users" :key="user.id">
            <td>{{ user.id }}</td>
            <td>{{ user.name }}</td>
            <td>{{ user.salary }}</td>
            <td>{{ user.age }}</td>
            <td>
              <button @click="removeWorker(user.id)" class="remove-button">Удалить</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'Jaden', salary: 19000, age: 22 },
        { id: 2, name: 'Vinnie', salary: 2500, age: 23 },
        { id: 3, name: 'Josh', salary: 3100, age: 25 },
      ],
    };
  },
  methods: {
    removeWorker(id) {
      this.users = this.users.filter(user => user.id !== id);
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(255, 163, 208);
  border: 2px solid rgb(207, 19, 113);
  border-radius: 10px;
  padding: 20px;
  max-width: 600px;
  margin: auto;
}

.task {
  background-color:rgb(255, 202, 218);
  border-radius: 5px;
}

h2 {
  text-align: center;
  color:rgb(199, 15, 107);
}

h3 {
  color: #cc0066;
}

.worker-table {
  width: 100%;
  border-collapse: collapse; /* Убираем двойные границы */
}

.worker-table th,
.worker-table td {
  border: 1px solid rgb(255, 217, 236); /* Розовые границы для ячеек */
  padding: 10px; /* Внутренние отступы */
}

.worker-table th {
  background-color:rgb(255, 180, 218); /* Цвет фона заголовков */
}

.remove-button {
  background-color: #ff3399;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px;
}

.remove-button:hover {
  background-color: #cc0066; /* Эффект при наведении на кнопку */
}
</style>