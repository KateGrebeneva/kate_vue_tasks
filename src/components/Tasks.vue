<template>
  <div class="container">
    <h1 class="title">Введите номер дня недели (0 - Воскресенье, 6 - Суббота)</h1>
    <input type="number" v-model="dayNumber" min="0" max="6" class="input" />
    <button @click="showDayName" class="button">Показать название дня</button>
    <h2 v-if="dayName" class="result">Сегодня: {{ dayName }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dayNumber: null,
      dayName: '',
    };
  },
  methods: {
    // Вспомогательный метод для получения названия дня недели
    getDayName(dayNumber) {
      const days = [
        'Воскресенье',
        'Понедельник',
        'Вторник',
        'Среда',
        'Четверг',
        'Пятница',
        'Суббота',
      ];
      return days[dayNumber] || 'Некорректный номер';
    },
    // Основной метод для отображения названия дня
    showDayName() {
      this.dayName = this.getDayName(this.dayNumber);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color: #f8e1f4; 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D; 
  font-family: 'Arial', sans-serif;
  font-size: 24px;
  margin-bottom: 20px;
}

.input {
  padding: 10px;
  border: 2px solid #D5006D; 
  border-radius: 5px;
  margin-bottom: 20px;
}

.button {
  background-color: #D5006D; 
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s;
}

.button:hover {
  background-color: #a4004e; 
  transform: scale(1.05);
}

.result {
  color: #D5006D; 
  font-size: 20px;
}
</style>
