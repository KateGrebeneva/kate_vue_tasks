<template>
  <div class="task-1">
    <h2>Задание 1</h2>
    <textarea v-model="text" placeholder="Введите текст..."></textarea>
    <p>Выводимый текст: {{ text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',
    };
  },
};
</script>

<style scoped>
.task-1 {
  background-color:rgb(255, 165, 209); /* Нежно-розовый фон */
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(255, 95, 175); /* Ярко-розовая граница */
  color: #333;
  max-width: 400px;
  margin: 20px auto;
  color:rgb(202, 0, 101);
}
textarea {
  width: 100%;
  height: 100px;
  padding: 10px;
  border-radius: 5px;
  border: 2px solid #ff69b4; /* Ярко-розовая граница */
  resize: none; /* Отключаем изменение размера */
}
textarea::placeholder {
  color: #ff1493; /* Цвет плейсхолдера */
}
p {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
</style>