<template>
  <div class="container">
    <h1 class="title">Сумма чисел</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num1: 1,
      num2: 2,
    };
  },
  mounted() {
    this.showSum();
  },
  methods: {
    showSum() {
      const sum = this.num1 + this.num2;
      alert("Сумма чисел: " + sum);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color:rgb(255, 168, 233);
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

body {
  background-color:rgb(255, 184, 226); 
}
</style>