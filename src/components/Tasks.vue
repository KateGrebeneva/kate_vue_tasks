<template>
  <div class="task-1">
    <h2>Задание 1</h2>
    <input v-model="message" placeholder="Введите текст">
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'hello',
    };
  },
};
</script>

<style scoped>
.task-1 {
  background-color:rgb(255, 155, 205);
  padding: 20px;
  border-radius: 10px;
  color: white;
}
input {
  padding: 10px;
  border-radius: 5px;
  border: none;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
p, h2 {
  font-size: 18px;
  margin-top: 10px;
  color:rgb(202, 0, 101);
}
</style>