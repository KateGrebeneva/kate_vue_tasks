<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref } from 'vue';
import UserForm from './components/UserForm.vue';
import Employee from './components/Employee.vue';

const users = ref([]);

const add = (name, surn) => {
  let id = users.value.length + 1;
  users.value.push({ id, name, surn });
};

const change = (id, name, surn) => {
  users.value = users.value.map(user => {
    if (user.id === id) {
      user.name = name;
      user.surn = surn;
    }
    return user;
  });
};
</script>

<template>
  <header>
  <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  <div class="container">
    <h1 class="title">Добавить пользователя</h1>
    <UserForm @add="add" />
    <h2 class="subtitle">Список пользователей</h2>
    <div class="user-list">
      <Employee
        v-for="user in users"
        :key="user.id"
        :id="user.id"
        :name="user.name"
        :surn="user.surn"
        @change="change"
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
  background-color:rgb(250, 189, 223); /* Светлый фон */
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