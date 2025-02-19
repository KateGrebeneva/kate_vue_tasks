<template>
  <div class="number-list-container">
    <h1 class="title">Список чисел от 1 до 30</h1>
    <p v-for="num in 30" :key="num" class="number-item">
      {{ num }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'NumberList',
};
</script>

<style scoped>
.number-list-container {
  background-color:rgb(247, 194, 225); 
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  color: #d5006d; 
  text-align: center;
  font-family: 'Arial', sans-serif; 
  margin-bottom: 20px;
}

.number-item {
  color: #d5006d; 
  font-size: 18px; 
  margin: 5px 0; 
  transition: transform 0.2s; 
}

.number-item:hover {
  transform: scale(1.1); 
}
</style>