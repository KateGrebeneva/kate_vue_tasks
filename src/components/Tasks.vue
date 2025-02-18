<template>
  <div class="container">
    <button @click="toggleVisibility" class="toggle-button">
      {{ isVisible ? 'Скрыть' : 'Показать' }} абзац
    </button>
    
    <p v-show="isVisible" class="paragraph">
      «Мы тут все сумасшедшие». Чеширский кот, «Алиса в стране чудес».
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false, // Начальное состояние видимости абзаца
    };
  },
  methods: {
    toggleVisibility() {
      this.isVisible = !this.isVisible; // Переключаем видимость
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
  background-color: #ffccdd; /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.toggle-button {
  background-color: #d5006d; /* Темно-розовая кнопка */
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  font-size: 18px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.toggle-button:hover {
  background-color: #a2004d; /* Более темный оттенок при наведении */
  transform: scale(1.05); /* Увеличение кнопки при наведении */
}

.paragraph {
  color: #800024; /* Темно-розовый цвет текста */
  font-size: 16px;
  margin-top: 20px;
  line-height: 1.5;
  transition: opacity 0.5s ease; /* Плавный переход для отображения */
}
</style>
