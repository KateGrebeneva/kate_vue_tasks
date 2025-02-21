<template>
  <div class="container">
    <!-- Задание 1: Селект для выбора дня недели -->
    <h2>Task#50 №1: Выберите день недели</h2>
    <select v-model="selectedDay" class="custom-select">
      <option v-for="day in days" :key="day">{{ day }}</option>
    </select>
    <p class="result">Выбранный день: <strong>{{ selectedDay }}</strong></p>

    <!-- Задание 2: Селекты для выбора дня, месяца и года -->
    <h2>Task#50 №2: Выберите дату</h2>
    <div class="date-selectors">
      <select v-model="selectedDate" class="custom-select">
        <option v-for="day in days" :key="day">{{ day }}</option>
      </select>
      <select v-model="selectedMonth" class="custom-select">
        <option v-for="month in months" :key="month">{{ month }}</option>
      </select>
      <select v-model="selectedYear" class="custom-select">
        <option v-for="year in years" :key="year">{{ year }}</option>
      </select>
    </div>
    <p class="result">Выбрано: {{ selectedDate }} {{ selectedMonth }} {{ selectedYear }}</p>

    <!-- Задание 3: Установка текущей даты по умолчанию -->
    <h2>Task#50 №3: Выберите текущую дату</h2>
    <div class="date-selectors">
      <select v-model="selectedDate" class="custom-select">
        <option v-for="day in days" :key="day">{{ day }}</option>
      </select>
      <select v-model="selectedMonth" class="custom-select">
        <option v-for="month in months" :key="month">{{ month }}</option>
      </select>
      <select v-model="selectedYear" class="custom-select">
        <option v-for="year in years" :key="year">{{ year }}</option>
      </select>
    </div>
    <p class="result">Выбрано: {{ selectedDate }} {{ selectedMonth }} {{ selectedYear }}</p>
  </div>
</template>

<script>
export default {
  data() {
    const currentDate = new Date();
    const currentDay = currentDate.getDate();
    const currentMonth = currentDate.getMonth();
    const currentYear = currentDate.getFullYear();

    return {
      // Задание 1
      selectedDay: 'Понедельник',
      days: ['Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота', 'Воскресенье'],

      // Задание 2
      selectedDate: currentDay,
      selectedMonth: currentMonth + 1, // месяцы с 0 до 11
      selectedYear: currentYear,
      months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      
      // Генерация годов (например, от 1900 до текущего года)
      years: Array.from({ length: currentYear - 1899 }, (_, i) => currentYear - i)
    };
  }
}
</script>

<style scoped>
.container {
  background-color:rgb(255, 158, 205);
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(239, 63, 151);
  max-width: 600px;
  margin: auto;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

h2 {
  color:rgb(214, 8, 111);
  text-align: center;
}

.custom-select {
  width: calc(33% - 10px);
  padding: 10px;
  margin: 15px 5px;
  border-radius: 5px;
  border: 1px solid rgb(209, 8, 109);
  background-color: #fff;
  font-size: 16px;
}

.date-selectors {
  display: flex;
  justify-content: space-between;
}

.result {
  color:rgb(211, 12, 112);
  font-size: 18px;
  text-align: center;
}
</style>