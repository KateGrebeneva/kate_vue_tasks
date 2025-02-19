<template>
  <div class="container">
    <h1 class="title">Однажды в сказке</h1>
    <p class="description">Это история о том, как магия и реальность переплетаются в мире сказок.</p>
    <div class="character">
      <h2 class="character-title">Главные персонажи</h2>
      <ul class="character-list">
        <li>Эмма Свон</li>
        <li>Румпельштильцхен</li>
        <li>Регина Миллс</li>
        <li>Киллиан Джемс</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OnceUponATime',
};
</script>

<style scoped>
.container {
  background-color:rgb(123, 0, 18); /* Бордовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  margin: 20px;
}

.title {
  color: #f9d5d3; /* Светлый оттенок для заголовка */
  text-align: center;
  font-size: 2em;
  margin-bottom: 10px;
}

.description {
  color: #f9d5d3; /* Светлый текст для описания */
  font-size: 1.2em;
  text-align: center;
  margin-bottom: 20px;
}

.character {
  border: 2px solid rgb(248, 171, 167); /* Светлая граница */
  border-radius: 10px;
  padding: 15px;
   background-color:rgba(180, 35, 57, 0.84);
}

.character-title {
  color:rgb(245, 141, 136); /* Светлый цвет для заголовка персонажей */
  text-align: center;
}

.character-list {
  list-style-type: none; /* Убираем маркеры списка */
  padding: 0; /* Убираем отступы */
}

.character-list li {
  color:rgb(255, 191, 188); /* Цвет для элементов списка */
  font-size: 1.1em;
  margin: 5px 0; /* Отступы между элементами списка */
}
</style>