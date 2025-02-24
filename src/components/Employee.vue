<template>
  <div class="employee-container">
    <h2 class="employee-title">Employee Information</h2>
    <p class="employee-name">Name: {{ name }}</p>
    <p class="employee-surname">Surname: {{ surn }}</p>
    <p class="employee-age">Age: {{ age }}</p>
  </div>
</template>

<script>
export default {
  props: ['name', 'surn', 'age']
}
</script>

<style scoped>
.employee-container {
  background-color:rgb(254, 192, 222);
  border: 2px solid rgb(218, 54, 136);
  border-radius: 10px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.employee-title {
  color:rgb(213, 0, 107);
}

.employee-name, .employee-surname, .employee-age {
  font-size: 16px;
  font-weight: bold;
  color:rgb(244, 31, 134);
}
</style>