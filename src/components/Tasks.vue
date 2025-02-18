<template>
  <div class="container">
    <button @click="toggleVisibility" class="toggle-button">
      {{ isVisible ? 'Скрыть' : 'Показать' }} абзацы
    </button>
    
    <template v-if="isVisible">
      <p class="paragraph">Ежик — это один из персонажей мультсериала "Смешарики", который отличается своей добротой и умом.</p>
      <p class="paragraph">Он всегда готов прийти на помощь своим друзьям и решать возникающие проблемы.</p>
      <p class="paragraph">Ежик любит природу и часто проводит время на свежем воздухе, исследуя окружающий мир.</p>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true, // Начальное состояние видимости абзацев
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
  transition: background-color 0.3s ease;
}

.toggle-button:hover {
  background-color: #a2004d; /* Более темный оттенок при наведении */
}

.paragraph {
  color: #800024; /* Темно-розовый цвет текста */
  font-size: 16px;
  margin: 10px 0;
  line-height: 1.5;
}

.paragraph:nth-child(even) {
  font-style: italic; /* Курсив для четных абзацев */
}

.paragraph:nth-child(odd) {
  font-weight: bold; /* Жирный шрифт для нечетных абзацев */
}
</style>