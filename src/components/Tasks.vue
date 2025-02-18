<template>
  <div class="container">
    <button @click="handleClick" :disabled="isClicked" class="click-button">
      {{ isClicked ? 'Клик выполнен' : 'Нажми на меня' }}
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClicked: false // Флаг, отслеживающий, был ли клик
    };
  },
  methods: {
    handleClick() {
      if (!this.isClicked) {
        console.log('Первый клик по кнопке!');
        this.isClicked = true; // Устанавливаем флаг в true после первого клика
      }
    }
  }
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
}

.click-button {
  padding: 15px 25px;
  border: none;
  border-radius: 5px;
  background-color: rgb(208, 47, 130);
  color: white;
  font-size: 1em;
  cursor: pointer;
}

.click-button:disabled {
  background-color: rgba(208, 47, 130, 0.5);
  cursor: not-allowed;
}
</style>