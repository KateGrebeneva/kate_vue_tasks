<template>
  <div class="container">
    <h1 class="title">Текущая дата</h1>
  </div>
</template>

<script>
export default {
  mounted() {
    this.showDate();
  },
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
  background-color:rgb(247, 203, 235); 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.title {
  color: #D5006D;
  font-family: 'Arial', sans-serif;
}
</style>
