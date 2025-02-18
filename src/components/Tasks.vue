<template>
  <div class="container">
    <p v-if="isAdmin" class="admin-message">Вы администратор! У вас есть доступ к полным функциям.</p>
    <p v-else class="user-message">Вы обычный пользователь. Ваши возможности ограничены.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAdmin: true, // Измените на false, чтобы увидеть другое сообщение
    };
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
}

.admin-message {
  color: white;
  background-color: #d5006d; /* Темно-розовый фон */
  padding: 20px;
  border-radius: 10px;
  font-size: 24px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s, background-color 0.3s;
}

.admin-message:hover {
  transform: scale(1.05);
  background-color: #c51162; /* Более светлый оттенок при наведении */
}

.user-message {
  color: white;
  background-color: #ff4081; /* Светло-розовый фон */
  padding: 20px;
  border-radius: 10px;
  font-size: 24px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s, background-color 0.3s;
}

.user-message:hover {
  transform: scale(1.05);
  background-color: #f50057; /* Более светлый оттенок при наведении */
}
</style>
