<template>
  <div class="container">
    <!-- Задание №1 -->
    <h2>Задание №1: Выбор родного языка</h2>
    <div class="radio-group">
      <label>
        <input type="radio" v-model="choice" value="Русский"> Русский
      </label>
      <label>
        <input type="radio" v-model="choice" value="Английский"> Английский
      </label>
      <label>
        <input type="radio" v-model="choice" value="Испанский"> Испанский
      </label>
    </div>
    <p>Вы выбрали: {{ choice }}</p>

    <!-- Задание №2 -->
    <h2>Задание №2: Фраза на выбранном языке</h2>
    <div class="radio-group">
      <label>
        <input type="radio" v-model="language" value="Русский"> Русский
      </label>
      <label>
        <input type="radio" v-model="language" value="Английский"> Английский
      </label>
      <label>
        <input type="radio" v-model="language" value="Испанский"> Испанский
      </label>
    </div>
    <p v-if="language === 'Русский'">Привет! Как дела?</p>
    <p v-if="language === 'Английский'">Hello! How are you?</p>
    <p v-if="language === 'Испанский'">¡Hola! ¿Cómo estás?</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      choice: '',
      language: ''
    }
  }
}
</script>

<style scoped>
.container {
  background-color:rgb(255, 131, 177);
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(255, 43, 135);
}

h2 {
  color:rgb(216, 21, 119);
}

.radio-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin: 5px 0;
  font-weight: bold;
}

p {
  color:rgb(216, 21, 119);
  font-size: 18px;
}
</style>