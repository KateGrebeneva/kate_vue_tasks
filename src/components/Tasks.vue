<template>
  <div class="container">
    <h2>Вопрос: В каком городе вы живете?</h2>
    <select v-model="selected" class="city-select">
      <option value="Симферополь">Симферополь</option>
      <option value="Ялта">Ялта</option>
      <option value="Керчь">Керчь</option>
      <option value="Алушта">Алушта</option>
      <option value="Севастополь">Севастополь</option>
    </select>
    
    <p class="result">Вы живете в городе: <strong>{{ selected }}</strong></p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: 'Симферополь' // значение по умолчанию
    }
  }
}
</script>

<style scoped>
.container {
  background-color:rgb(255, 153, 185);
  padding: 20px;
  border-radius: 10px;
  border: 2px solid rgb(227, 25, 126);
  max-width: 400px;
  margin: auto;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

h2 {
  color:rgb(247, 37, 142);
  text-align: center;
}

.city-select {
  width: 100%;
  padding: 10px;
  margin: 15px 0;
  border-radius: 5px;
  border: 1px solidrgb(219, 12, 115);
  background-color: #fff;
  font-size: 16px;
}

.result {
  color:rgb(219, 20, 119);
  font-size: 18px;
  text-align: center;
}
</style>