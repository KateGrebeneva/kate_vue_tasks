<template>
  <div class="checkbox-container">
    <input type="checkbox" v-model="checked" id="checkbox">
    <label for="checkbox">Отобразить абзац</label>
    <p v-if="checked" class="visible-paragraph">Вы отметили чекбокс! Да!</p>
    <p v-else class="hidden-paragraph">Чекбокс не отмечен. Нет.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checked: false, // Начальное состояние чекбокса
    };
  },
};
</script>

<style scoped>
.checkbox-container {
  background-color:rgb(255, 143, 189); /* Нежно-розовый фон */
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(255, 70, 163); /* Ярко-розовая граница */
  color: #333;
  max-width: 400px;
  margin: 20px auto;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Легкая тень */
}

input[type="checkbox"] {
  cursor: pointer; /* Указатель при наведении */
}

label {
  margin-left: 10px; /* Отступ между чекбоксом и текстом */
  font-size: 18px; /* Размер шрифта для текста */
}

.visible-paragraph {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(26, 160, 26); /* Зеленый цвет для видимого абзаца */
}

.hidden-paragraph {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(125, 0, 0); /* Бордовый цвет для скрытого абзаца */
}
</style>