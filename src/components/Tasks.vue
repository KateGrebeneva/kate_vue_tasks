<template>
  <div class="container">
    <h1 class="title">Текущая дата</h1>
    <button @click="showDate" class="date-button">Показать текущую дату</button>
  </div>
</template>

<script>
export default {
  methods: {
    showDate() {
      const currentDate = new Date().toLocaleString();
      alert("Текущая дата и время: " + currentDate);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color:rgb(246, 180, 230); 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D; 
  font-family: 'Arial', sans-serif;
  margin-bottom: 15px;
}

.date-button {
  background-color: #D5006D; 
  color: white; 
  border: none; 
  padding: 10px 20px; 
  border-radius: 5px; 
  cursor: pointer; 
  font-size: 1em; 
}

.date-button:hover {
  background-color: #B0004C;
}
</style>

