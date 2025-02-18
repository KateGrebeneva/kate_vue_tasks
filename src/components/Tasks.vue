<template>
  <div class="container">
    <h2 class="title">Вывод ключей и элементов массива</h2>
    <ul class="item-list">
      <li v-for="(elem, key) in arr" :key="key" class="item">
        №{{ key + 1 }}: {{ elem }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z'],
    };
  },
};
</script>

<style scoped>
.container {
  background-color: #ffccdd; /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  color: #d5006d; /* Темно-розовый заголовок */
  text-align: center;
  margin-bottom: 20px;
}

.item-list {
  list-style-type: none; /* Убираем стандартные маркеры списка */
  padding: 0; /* Убираем отступы */
}

.item {
  background-color: #f8b2c4; /* Более светлый розовый для элементов списка */
  color: #800024; /* Темно-розовый текст */
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  transition: transform 0.2s, background-color 0.3s; /* Плавные переходы */
}

.item:hover {
  transform: scale(1.05); /* Увеличение элемента при наведении */
  background-color: #ff99b5; /* Изменение фона при наведении */
}
</style>