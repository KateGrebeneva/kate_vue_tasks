<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref } from 'vue'
import Employee from './components/Employee.vue';

const users = ref([
  { id: 1, name: 'Piter', surn: 'Pen' },
  { id: 2, name: 'Cora', surn: 'Mills' },
  { id: 3, name: 'Regina', surn: 'Mills' },
]);

const remove = (id) => {
  users.value = users.value.filter(user => user.id !== id);
};
</script>

<template>
  <header>
  <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  <div class="container">
      <h1 class="title">Список пользователей</h1>
      <div class="user-list">
        <Employee
          v-for="user in users"
          :key="user.id"
          :id="user.id"
          :name="user.name"
          :surn="user.surn"
          @remove="remove"
        />
     </div>
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
.container {
  padding: 20px;
  background-color:rgb(255, 208, 235); /* Светлый фон */
  border-radius: 10px; /* Скругленные углы */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Тень */
}

.title {
  color: rgb(250, 62, 156); /* Розовый цвет заголовка */
  text-align: center;
}

.user-list {
  margin-top: 20px;
}
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}


.message-box {
  margin-top: 1rem; /* Отступ сверху */
  padding: 10px; /* Внутренний отступ */
  border: 2px solid rgb(250, 62, 156); /* Розовая рамка */
  background-color: rgba(250, 62, 156, 0.1); /* Светлый розовый фон */
  color: rgb(250, 62, 156); /* Розовый цвет текста */
  border-radius: 8px; /* Скругленные углы */
}

@media (min-width: 1024px) {
  header {
    display: flex;
    align-items: center; 
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    align-items: flex-start; 
    flex-wrap: wrap;
  }
}
</style>