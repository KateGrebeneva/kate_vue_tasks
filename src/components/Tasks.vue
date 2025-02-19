<template>
  <div class="container">
    <h1 class="title">Статус задачи</h1>
    <p :class="{ done: obj.done, selected: obj.selected }">Текущий статус задачи</p>
    <button class="button" @click="toggleStatus">Переключить статус</button>
  </div>
</template>

<script>
export default {
  name: 'TaskStatus',
  data() {
    return {
      obj: {
        done: true,      // Класс будет применен
        selected: false, // Класс не будет применен
      },
    };
  },
  methods: {
    toggleStatus() {
      // Переключаем значение done для демонстрации
      this.obj.done = !this.obj.done;
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(246, 164, 197); /* Нежно-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  margin: 20px;
}

.title {
  color: #d5006d; /* Темно-розовый цвет для заголовка */
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 15px;
}

p {
  font-size: 1.2em;
  text-align: center;
}

/* Классы для применения */
.done {
  color: #4caf50; /* Зеленый цвет для завершенной задачи */
  font-weight: bold; /* Жирное начертание текста */
}

.selected {
  text-decoration: underline; /* Подчеркивание для выбранной задачи */
  color: #ff4081; /* Яркий розовый цвет */
}

.button {
  background-color: #d5006d; /* Темно-розовая кнопка */
  color: white;
  border: none;
  border-radius: 25px; /* Плавные линии */
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s; /* Плавный переход */
}

.button:hover {
  background-color: #a0004c; /* Более темный оттенок при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}
</style>