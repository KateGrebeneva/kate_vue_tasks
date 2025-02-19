<template>
  <div class="container">
    <h1 class="title">Перебор объектов</h1>

    <div class="task">
      <h2 class="task-title">Задание №3</h2>
      <ul class="item-list">
        <li class="item" v-for="(elem, key, index) in obj" :key="key">
          {{ key }} - {{ elem }} - {{ index }}
        </li>
      </ul>
    </div>

    <div class="task">
      <h2 class="task-title">Задание №4</h2>
      <ul class="item-list">
        <li class="item" v-for="(elem, key, index) in obj" :key="key">
          {{ key }} - {{ elem }} - {{ index + 1 }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        user1: '100$',
        user2: '200$',
        user3: '300$',
      },
    };
  },
};
</script>

<style scoped>
.container {
  background-color: #ffccdd; /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  color: #d5006d; /* Темно-розовый заголовок */
  text-align: center;
  margin-bottom: 20px;
}

.task {
  margin-bottom: 30px;
}

.task-title {
  color: #d5006d; /* Темно-розовый заголовок задания */
  margin-bottom: 10px;
}

.item-list {
  list-style-type: none; /* Убираем стандартные маркеры списка */
  padding: 0; /* Убираем отступы */
}

.item {
  background-color: #f8b2c4; /* Более светлый розовый для элементов списка */
  color: #800024; /* Темно-розовый текст */
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  transition: transform 0.2s, background-color 0.3s; /* Плавные переходы */
}

.item:hover {
  transform: scale(1.05); /* Увеличение элемента при наведении */
  background-color: #ff99b5; /* Изменение фона при наведении */
}
</style>
