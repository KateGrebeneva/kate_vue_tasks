<template>
  <div class="container">
    <p v-if="day === 'Понедельник'" class="day-message">Понедельник</p>
    <p v-if="day === 'Вторник'" class="day-message">Вторник</p>
    <p v-if="day === 'Среда'" class="day-message">Среда</p>
    <p v-if="day === 'Четверг'" class="day-message">Четверг</p>
    <p v-if="day === 'Пятница'" class="day-message">Пятница</p>
    <p v-if="day === 'Суббота'" class="day-message">Суббота</p>
    <p v-if="day === 'Воскресенье'" class="day-message">Воскресенье</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      day: 'Вторник', 
    };
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
}

.day-message {
  color: white;
  background-color: #d5006d; /* Темно-розовый фон */
  padding: 20px;
  border-radius: 10px;
  font-size: 24px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s, background-color 0.3s;
}

.day-message:hover {
  transform: scale(1.05);
  background-color: #c51162; /* Более светлый оттенок при наведении */
}
</style>