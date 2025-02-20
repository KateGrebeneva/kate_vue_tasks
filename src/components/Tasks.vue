<template>
  <div class="task-2">
    <h2>Задание 2</h2>
    <textarea v-model="text" placeholder="Введите текст..." ></textarea>
    <button @click="getWords">Получить слова</button>
     <ul>
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',        // для привязки текста
      words: [],       // массив для хранения слов
    };
  },
  methods: {
    getWords() {
      // Разбиваем текст на массив слов
      this.words = this.text.split(/\s+/).filter(Boolean);
    },
  },
};
</script>

<style scoped>
.task-2 {
  background-color:rgb(255, 162, 197); /* Нежно-розовый фон */
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(255, 76, 166); /* Ярко-розовая граница */
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
  border: 2px solidrgb(253, 90, 171); /* Ярко-розовая граница */
  color:rgb(202, 0, 101);
}
textarea::placeholder {
  color: #ff1493; /* Цвет плейсхолдера */
}
button {
  padding: 10px;
  background-color: #ff69b4; /* Ярко-розовая кнопка */
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
}
button:hover {
  background-color: #ff1493; /* Цвет кнопки при наведении */
}
ul {
  list-style-type: none; /* Убираем маркеры списка */
  padding-left: 0; /* Убираем отступ слева */
}
li {
  background-color: #fff; /* Белый фон для элементов списка */
  margin-top: 5px;
  padding: 5px;
  border-radius: 5px;
}
</style>


