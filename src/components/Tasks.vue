<template>
  <div class="container">
    <button @click="show" class="styled-button" v-if="!visible">Показать текст</button>
    <p v-if="visible" class="styled-text">Это текст, который изначально скрыт.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false, // Изначально скрыт
    };
  },
  methods: {
    show() {
      this.visible = true; // Показываем текст
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center; /* Центрируем содержимое */
  margin-top: 50px; /* Отступ сверху */
}

.styled-text {
  color: #d5006d; /* Темно-розовый цвет текста */
  font-size: 24px; /* Размер шрифта */
  font-weight: bold; /* Жирный шрифт */
  text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3); /* Тень текста */
  transition: opacity 0.5s; /* Плавный переход для появления текста */
}

.styled-button {
  background-color: #d5006d; /* Темно-розовый цвет фона */
  color: white; /* Цвет текста */
  border: none; /* Убираем рамку */
  border-radius: 8px; /* Закругленные углы */
  padding: 12px 24px; /* Отступы внутри кнопки */
  font-size: 18px; /* Размер шрифта на кнопке */
  cursor: pointer; /* Курсор в виде указателя */
  transition: background-color 0.3s, transform 0.2s; /* Плавный переход для фона и эффекта нажатия */
}

.styled-button:hover {
  background-color: #c51162; /* Более темный оттенок при наведении */
}

.styled-button:active {
  transform: scale(0.95); /* Эффект сжатия при нажатии */
}
</style>