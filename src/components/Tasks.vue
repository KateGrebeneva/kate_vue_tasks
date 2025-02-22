<template>
  <div class="container">
    <h2>Работники</h2>
    
    <div class="task" id="remove-worker-task">
      <h3>Задание 56: Удаление и редактирование работника</h3>
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
            <td>
              <template v-if="!user.isEdit">
                {{ user.name }}
                <button @click="edit(user)" class="edit-button">Редактировать</button>
              </template>
              <template v-else>
                <input v-model="user.name" />
                <button @click="save(user)" class="save-button">Сохранить</button>
              </template>
            </td>
            <td>
              <template v-if="!user.isEdit">
                {{ user.salary }}
              </template>
              <template v-else>
                <input v-model="user.salary" type="number" />
              </template>
            </td>
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
        { id: 1, name: 'Jaden', salary: 19000, age: 22, isEdit: false },
        { id: 2, name: 'Vinnie', salary: 2500, age: 23, isEdit: false },
        { id: 3, name: 'Josh', salary: 3100, age: 25, isEdit: false },
      ],
    };
  },
  methods: {
    edit(user) {
      user.isEdit = true;
    },
    save(user) {
      user.isEdit = false;
    },
    removeWorker(id) {
      this.users = this.users.filter(user => user.id !== id);
    },
  },
};
</script>

<style scoped>
.container {
  background-color: rgb(255, 163, 208);
  border: 2px solid rgb(207, 19, 113);
  border-radius: 10px;
  padding: 20px;
  max-width: 700px;
  margin: auto;
}

.task {
  background-color: rgb(255, 202, 218);
  border-radius: 5px;
}

h2 {
  text-align: center;
  color: rgb(199, 15, 107);
}

h3 {
  color: #cc0066;
}

.worker-table {
  width: 100%;
  border-collapse: collapse;
}

.worker-table th,
.worker-table td {
  border: 1px solid rgb(255, 217, 236);
  padding: 10px;
}

.worker-table th {
  background-color: rgb(255, 180, 218);
}

.edit-button,
.save-button {
  background-color: #ff3399;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px;
}

.edit-button:hover,
.save-button:hover {
  background-color: #cc0066; 
}

.remove-button {
  background-color: #ff3399;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px;
}

.remove-button:hover {
  background-color: #cc0066; 
}
</style>