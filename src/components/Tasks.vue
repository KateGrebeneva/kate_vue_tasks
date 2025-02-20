<template>
  <div class="container">
    <p :class="{ valid: isValid, disabled: isDisabled }">
      CSS класс -  isValid: false
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isValid: false,   
      isDisabled: true 
    };
  }
};
</script>

<style scoped>
.container {
  background-color:rgb(255, 207, 230); /* Светло-розовый фон */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

p {
  font-size: 20px;
  font-family: 'Arial', sans-serif;
  transition: all 0.3s ease; /* Плавный переход для стилей */
}

.valid {
  color: #d5006d; /* Зеленый цвет для валидного состояния */
  font-weight: bold; /* Жирный текст для валидного состояния */
}

.disabled {
  color:rgb(151, 11, 1); /* Красный цвет для отключенного состояния */
  text-decoration: line-through; /* Зачеркнутый текст для отключенного состояния */
}
</style>