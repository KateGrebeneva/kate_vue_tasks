<template>
  <div class="container">
    <h2>Блокировка элементов в Vue</h2>

    <div class="task" id="task-1">
      <h3>Задание №1</h3>
      <input type="text" v-bind:disabled="isInputDisabled" placeholder="Введите текст" />
      <button @click="toggleInput">Toggle Input</button>
    </div>

    <div class="task" id="task-2">
      <h3>Задание №2</h3>
      <input type="checkbox" v-model="isCheckboxChecked" /> Разрешить ввод
      <input type="text" v-bind:disabled="!isCheckboxChecked" placeholder="Введите текст" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isInputDisabled: true,
      isCheckboxChecked: false,
    };
  },
  methods: {
    toggleInput() {
      this.isInputDisabled = !this.isInputDisabled;
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(253, 191, 221);
  border: 2px solidrgb(255, 101, 178);
  border-radius: 10px;
  padding: 20px;
  max-width: 400px;
  margin: auto;
}

.task {
  background-color:rgb(255, 222, 233);
  border: 1px solid #ff66b2;
  border-radius: 5px;
  padding: 15px;
  margin-bottom: 20px;
}

h2 {
  text-align: center;
  color:rgb(214, 0, 107);
}

h3 {
  color: #cc0066;
}

button {
  background-color:rgb(249, 82, 166);
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px;
  cursor: pointer;
}

button:hover {
  background-color: #ff3399;
}

input[type="text"] {
  width: calc(100% - 22px);
  padding: 10px;
  margin-top: 10px;
  border: 1px solidrgb(207, 29, 118);
  border-radius: 5px;
}

input[type="checkbox"] {
  margin-right: 10px;
}
</style>