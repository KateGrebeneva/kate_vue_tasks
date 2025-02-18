<template>
  <div class="container">
    <h1 class="title">Task#16 №1</h1>
    <a href="https://once-upon-a-time.fandom.com/ru/wiki/%D0%9E%D0%B4%D0%BD%D0%B0%D0%B6%D0%B4%D1%8B_%D0%B2_%D1%81%D0%BA%D0%B0%D0%B7%D0%BA%D0%B5" @click.prevent="handleClick" class="link-button">Кликни меня!</a>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick(event) {
      console.log('Ссылка была нажата, но переход не произошел');
    }
  }
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
  background-color: rgb(248, 165, 213); 
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  font-size: 2em;
  color: #d5006d; 
}

.link-button {
  padding: 15px 25px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color: rgb(208, 47, 130); 
  color: white;
  font-size: 1em;
  margin: 10px;
  text-decoration: none; /* Убираем подчеркивание */
  display: inline-block; /* Чтобы кнопка выглядела как кнопка */
  transition: background-color 0.3s, transform 0.2s; 
}

.link-button:hover {
  background-color: #c51162; 
  transform: scale(1.05); 
}
</style>
