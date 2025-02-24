<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref } from 'vue'
import Tasks from './components/Tasks.vue'

const message = ref('');

const handleShow = (param1, param2) => {
  message.value = param1 + " " + param2; // Сохраняем сообщение из события
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <Tasks @show="handleShow" />
    <div v-if="message" class="message-box">{{ message }}</div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
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