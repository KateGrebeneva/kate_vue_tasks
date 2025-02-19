<template>
  <div class="task-container">
    <!-- Задание 1 -->
    <div class="task">
      <h2 class="task-title">Задание №1</h2>
      <div v-for="elem in items" :key="elem" class="item-wrapper">
        <p class="item">{{ elem }}</p>
        <p class="divider">Winx</p>
      </div>
    </div>

    <div class="task">
      <h2 class="task-title">Задание №2</h2>
      <ul class="item-list">
        <template v-for="elem in items" :key="elem">
          <li class="item">{{ elem }}</li>
          <li class="divider">Bratz</li>
        </template>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
    };
  },
};
</script>

<style scoped>
.task-container {
  background-color:rgb(245, 187, 206); 
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.task {
  margin-bottom: 30px;
}

.task-title {
  color: #d5006d; 
  margin-bottom: 10px;
  font-family: 'Arial', sans-serif; 
  text-shadow: 1px 1px #fff; 
}

.item-wrapper {
  background-color: #f8b2c4; 
  padding: 10px;
  border-radius: 5px;
}

.item {
  color: #800024; 
  font-weight: bold; 
}

.divider {
  border-top: 1px solid #d5006d;
  margin-top: 5px;
  color:rgb(165, 0, 47);
}

.item-list {
  list-style-type: none; 
  padding: 0; 
}
</style>