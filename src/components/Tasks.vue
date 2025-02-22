<template>
  <div class="container">
    <!-- Задание №1 -->
    <div class="task" id="task-1">
      <h3>Задание №1: Добавление элемента в конец списка</h3>
      <input v-model="newItem" placeholder="Введите новый элемент" />
      <button @click="addItem">Добавить</button>
      <ul>
        <li v-for="(item, index) in items" :key="index">{{ item }}</li>
      </ul>
    </div>

    <!-- Задание №2 -->
    <div class="task" id="task-2">
      <h3>Задание №2: Добавление элемента в начало списка</h3>
      <input v-model="newItemForTask2" placeholder="Введите новый элемент" />
      <button @click="addItemToStart">Добавить в начало</button>
      <ul>
        <li v-for="(item, index) in itemsForTask2" :key="index">{{ item }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newItem: '',
      items: ['Swan', 'Cat', 'Dog'],
      newItemForTask2: '',
      itemsForTask2: ['Swan', 'Cat', 'Dog'],
    };
  },
  methods: {
    addItem() {
      if (this.newItem) {
        this.items.push(this.newItem);
        this.newItem = ''; // Очистка инпута после добавления
      }
    },
    addItemToStart() {
      if (this.newItemForTask2) {
        this.itemsForTask2.unshift(this.newItemForTask2);
        this.newItemForTask2 = ''; // Очистка инпута после добавления
      }
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(248, 164, 205);
  border: 2px solid rgb(254, 64, 159);
  border-radius: 10px;
  padding: 20px;
  max-width: 600px;
  margin: auto;
}

.task {
  background-color:rgb(250, 199, 216);
  border: 1px solid rgb(237, 61, 149);
  border-radius: 5px;
  padding: 15px;
  margin-bottom: 20px;
}

h2 {
  text-align: center;
  color: #ff3399;
}

h3 {
  color: #cc0066;
}

input[type="text"] {
  width: calc(100% - 22px);
  padding: 10px;
  margin-top: 10px;
  border: 1px solid #ff66b2;
  border-radius: 5px;
}

button {
  background-color: #ff3399;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px;
  cursor: pointer;
}

button:hover {
  background-color: #cc0066;
}

ul {
  list-style-type: none; 
  padding-left: 0; 
}

li {
  background-color: #fff; 
  margin: 5px 0; 
  padding: 10px; 
  border-radius: 5px; 
}
</style>