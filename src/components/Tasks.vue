<template>
  <div class="task-container">
    <!-- Задание 1 -->
    <div class="task">
      <h2 class="task-title">Задание №1: Персонажи из Смешариков</h2>
      <ul class="links-list">
        <li v-for="href in hrefs" :key="href.href" class="link-item">
          <a :href="href.href" class="link">{{ href.text }}</a>
        </li>
      </ul>
    </div>

    <!-- Задание 2 -->
    <div class="task">
      <h2 class="task-title">Задание №2: Список цветов</h2>
      <table class="products-table">
        <tr v-for="product in products" :key="product.name">
          <td>{{ product.name }}</td>
          <td>{{ product.price }}</td>
          <td>{{ product.quantity }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hrefs: [
        { href: '1.html', text: 'Крош' },
        { href: '2.html', text: 'Ёжик' },
        { href: '3.html', text: 'Нюша' },
      ],
      products: [
        { name: 'Роза', price: 100, quantity: 5 },
        { name: 'Тюльпан', price: 200, quantity: 4 },
        { name: 'Лилия', price: 300, quantity: 3 },
      ],
    };
  },
};
</script>

<style scoped>
.task-container {
  background-color: #ffccdd; /* Светло-розовый фон */
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.task {
  margin-bottom: 30px;
}

.task-title {
  color: #d5006d; /* Темно-розовый заголовок задания */
  margin-bottom: 10px;
  font-family: 'Arial', sans-serif; /* Шрифт заголовка */
  text-shadow: 1px 1px #fff; /* Тень для заголовка */
}

.links-list {
  list-style-type: none; /* Убираем стандартные маркеры списка */
  padding: 0; /* Убираем отступы */
}

.link-item {
  margin-bottom: 10px; /* Отступ между элементами списка */
}

.link {
  color: #d5006d; /* Темно-розовая ссылка */
  text-decoration: none; /* Убираем подчеркивание */
}

.link:hover {
  text-decoration: underline; /* Подчеркивание при наведении */
}

.products-table {
  width: 100%;
  border-collapse: collapse; /* Убираем промежутки между ячейками */
}

.products-table td {
  border: 1px solid #d5006d; /* Темно-розовая граница ячеек */
  padding: 10px;
   color:rgb(186, 6, 99);
}
</style>