<template>
  <div class="container">
    <h1 class="title">Управление видимостью текста</h1>
    <p :class="obj">{{ message }}</p>
    <div class="button-group">
      <button class="button" @click="showElement">Показать</button>
      <button class="button" @click="hideElement">Скрыть</button>
      <button class="button" @click="toggleElement">Тоггл</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VisibilityToggle',
  data() {
    return {
      message: 'Ариэль – жизнерадостная обитательница морских глубин.',
      obj: {
        hidden: true,
      },
    };
  },
  methods: {
    showElement() {
      this.obj.hidden = false;
    },
    hideElement() {
      this.obj.hidden = true;
    },
    toggleElement() {
      this.obj.hidden = !this.obj.hidden;
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(255, 187, 210); /* Нежно-розовый фон */
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
  font-size: 1.5em;
  text-align: center;
  color: #d5006d;
}

/* Класс для скрытия текста */
.hidden {
  display: none; /* Скрывает элемент */
}

.button-group {
  display: flex;
  justify-content: center;
  gap: 10px; /* Промежуток между кнопками */
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