<template>
  <div class="container">
    <h1 class="styled-text">Задание №1: Квадрат числа</h1>
    <p class="result">{{ num * num }}</p>

    <h1 class="styled-text">Задание №2: Сумма чисел</h1>
    <p class="result">{{ num1 + num2 + num3 }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 5,
      num1: 1,
      num2: 2,
      num3: 3,
    }
  }
}
</script>

<style scoped>
.container {
  text-align: center; 
  margin-top: 50px; 
}

.styled-text {
  color: #D5006D; 
  font-family: 'Arial', sans-serif; 
  font-size: 28px; 
  margin-bottom: 20px; 
}

.result {
  color:rgb(158, 0, 71); 
  background-color:rgba(242, 12, 131, 0.55); 
  font-family: 'Arial', sans-serif; 
  font-size: 24px; 
  padding: 10px; 
  border: 2px solid #D5006D; 
  border-radius: 8px; 
  display: inline-block; 
  transition: background-color 0.3s ease; 
}

.result:hover {
  background-color: rgba(213, 0, 109, 0.8); 
}
</style>

