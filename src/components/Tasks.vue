<template>
  <div class="container">
    <h2>Удаление элементов из списка в Vue</h2>

    <!-- Задание: Удаление элемента из списка -->
    <div class="task" id="remove-item-task">
      <h3>Персонажи из сериала "Сотня"</h3>
      <ul>
        <li v-for="(item, index) in items" :key="index" class="list-item">
          {{ item }}
          <button @click="removeItem(index)" class="remove-button">Удалить</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Беллами', 'Кларк', 'Октавия', 'Джаспер', 'Финн'],
    };
  },
  methods: {
    removeItem(index) {
      this.items.splice(index, 1);
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(254, 176, 214);
  border: 2px solid rgb(228, 38, 133);
  border-radius: 10px;
  padding: 20px;
  max-width: 600px;
  margin: auto;
}

.task {
  background-color:rgb(251, 195, 214);
  border: 1px solid rgb(228, 40, 134);
  border-radius: 5px;
  padding: 15px;
}

h2 {
  text-align: center;
  color: #ff3399;
}

h3 {
  color: #cc0066;
}

ul {
  list-style-type: none; /* Убираем маркеры */
  padding-left: 0; /* Убираем отступ слева */
}

.list-item {
  background-color: #fff; /* Белый фон для элементов списка */
  margin: 5px 0; /* Отступы между элементами списка */
  padding: 10px; /* Внутренние отступы */
  border-radius: 5px; /* Закругленные углы */
  display: flex; /* Используем flex для выравнивания кнопки */
  justify-content: space-between; /* Распределяем элементы по краям */
}

.remove-button {
  background-color: #ff3399;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;
}

.remove-button:hover {
  background-color: #cc0066; /* Эффект при наведении на кнопку */
}
</style>