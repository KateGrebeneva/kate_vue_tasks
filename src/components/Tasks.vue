<template>
  <div class="container">
    <h2 class="title">Элементы массива в виде списка</h2>
    <ul class="item-list">
      <li v-for="item in items" :key="item" class="item">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    };
  },
};
</script>

<style scoped>
.container {
  background-color: #ffccdd; /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
}

.title {
  color: #d5006d; /* Темно-розовый заголовок */
  text-align: center;
}

.item-list {
  list-style-type: none; /* Убираем стандартные маркеры списка */
}

.item {
  background-color: #f8b2c4; /* Более светлый розовый для элементов списка */
  color: #800024; /* Темно-розовый текст */
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
}
</style>