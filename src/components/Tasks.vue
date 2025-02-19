<template>
  <div class="container">
    <h2 class="title">Задание №3</h2>
    <ul class="list">
      <li v-for="(elem, index) in arr" :key="index" class="list-item">{{ elem }}</li>
    </ul>
    <button class="button" @click="removeLast">Удалить последний элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ['Music', 'Dance', 'Poetry'],
    };
  },
  methods: {
    removeLast() {
      this.arr.pop();
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(251, 172, 218); 
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
}

.title {
  color: #d5006d; 
  text-align: center;
}

.list {
  list-style-type: none; 
  padding: 0; 
}

.list-item {
  color: #d5006d;
  font-size: 18px; 
  margin: 10px 0;
  padding: 10px; 
  border: 2px solid #d5006d; 
  border-radius: 10px; 
}

.button {
  background-color: #d5006d; 
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px;
  cursor: pointer;
}

.button:hover {
  background-color: #b0004c; 
}
</style>