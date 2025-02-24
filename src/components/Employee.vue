<template>
  <div class="employee-container">
    <h2 class="employee-title">Employee List</h2>
    <ul class="employee-list">
      <li v-for="(employee, index) in arg" :key="index" class="employee-list-item">
        {{ employee }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    arg: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.employee-container {
  background-color:rgb(255, 174, 213);
  border: 2px solidrgb(225, 55, 140);
  border-radius: 10px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.employee-title {
  color:rgb(243, 52, 148);
  text-align: center;
}

.employee-list {
  list-style-type: none;
  padding: 0;
}

.employee-list-item {
  background-color:rgb(255, 214, 230);
  border: 1px solid rgb(248, 67, 157);
  border-radius: 5px;
  margin: 5px 0;
  padding: 10px;
  transition: background-color 0.3s;
}

.employee-list-item:hover {
  background-color:rgb(252, 138, 210);
}
</style>