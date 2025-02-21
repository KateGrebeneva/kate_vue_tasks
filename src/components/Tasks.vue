<template>
  <div class="container">
    <h2>Задание №1: Выбор языков</h2>
    <div class="checkbox-group">
      <label>
        <input type="checkbox" v-model="languages" value="JavaScript"> JavaScript
      </label>
      <label>
        <input type="checkbox" v-model="languages" value="Python"> Python
      </label>
      <label>
        <input type="checkbox" v-model="languages" value="Java"> Java
      </label>
      <label>
        <input type="checkbox" v-model="languages" value="C++"> C++
      </label>
    </div>

    <h2>Задание №2: Список языков</h2>
    <ul>
      <li v-for="(language, index) in languages" :key="index">{{ language }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [],
    }
  }
}
</script>

<style scoped>
.container {
  background-color:rgb(255, 134, 176);
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(209, 23, 88);
}

h2 {
  color:rgb(234, 27, 131);
}

.checkbox-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin: 5px 0;
  font-weight: bold;
}

ul {
  list-style-type: square;
  padding-left: 20px;
}

li {
  color:rgb(232, 24, 128);
}
</style>