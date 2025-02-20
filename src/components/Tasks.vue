<template>
  <div class="task-1">
    <h2>Задание 1</h2>
    <input v-model.number="num" placeholder="Введите число" />
    <button @click="calc">Получить квадратный корень</button>
    <p>Квадратный корень: {{ res }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      res: 0,
    };
  },
  methods: {
    calc() {
      this.res = Math.sqrt(this.num);
    },
  },
};
</script>

<style scoped>
.task-1 {
  background-color:rgb(254, 190, 229);
  padding: 20px;
  border-radius: 10px;
  border: 2px solidrgb(253, 132, 192);
  color: #333;
}
input {
  padding: 10px;
  border-radius: 5px;
  border: 2px solid #ff99cc;
  margin-right: 10px;
}
button {
  padding: 10px;
  background-color:rgb(255, 122, 188);
  border-color:rgb(135, 0, 67);
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #ff66b2;
}
p {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
h2{
  color:rgb(202, 0, 101);
}
</style>