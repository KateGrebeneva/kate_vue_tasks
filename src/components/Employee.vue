<template>
  <div class="employee-container">
    <h2 class="employee-title">Employee Information</h2>
    <p class="employee-name">{{ name }} - {{ position }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Hopper',
      position: 'Doctor'
    }
  }
}
</script>

<style scoped>
.employee-container {
  background-color:rgb(255, 156, 204);
  border: 2px solid rgb(192, 19, 105);
  border-radius: 10px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.employee-title {
  color:rgb(227, 13, 120);
}

.employee-name {
  font-size: 18px;
  font-weight: bold;
}
</style>