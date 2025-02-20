<template>
  <div class="task-3">
    <h2>Задание 3</h2>
    <input v-model="text1" placeholder="Введите текст в первый инпут" />
    <input v-model="text2" placeholder="Введите текст во второй инпут" />
    <button @click="swapText">Обменять текст</button>
    <p>Текст из первого инпута: {{ text1 }}</p>
    <p>Текст из второго инпута: {{ text2 }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text1: '',
      text2: '',
    };
  },
  methods: {
    swapText() {
      const temp = this.text1;
      this.text1 = this.text2;
      this.text2 = temp;
    },
  },
};
</script>

<style scoped>
.task-3 {
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
  background-color:rgb(248, 0, 124);
  border-color:rgb(135, 0, 67);
  border-radius: 5px;
  cursor: pointer;
  color:rgb(255, 202, 229);
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