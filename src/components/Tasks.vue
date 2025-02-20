<template>
  <div class="task-4">
    <h2>Задание 4</h2>
    <input v-model="fullName" placeholder="Введите ФИО через пробел" />
    <button @click="splitName">Разделить ФИО</button>
    <p>Фамилия: {{ lastName }}</p>
    <p>Имя: {{ firstName }}</p>
    <p>Отчество: {{ middleName }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: '',
      lastName: '',
      firstName: '',
      middleName: '',
    };
  },
  methods: {
    splitName() {
      const names = this.fullName.split(' ');
      this.lastName = names[0] || '';
      this.firstName = names[1] || '';
      this.middleName = names[2] || '';
    },
  },
};
</script>

<style scoped>
.task-4 {
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