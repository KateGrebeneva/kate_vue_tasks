<template>
  <div class="container">
    <h2>Модификаторы клавиш в Vue</h2>

    <!-- Задание №1 -->
    <div class="task" id="task-1">
      <h3>Задание №1: Ввод текста и вывод при нажатии Enter</h3>
      <input type="text" v-model="inputText" @keyup.enter="showText" placeholder="Введите текст и нажмите Enter" />
      <p class="output">{{ outputText }}</p>
    </div>

    <!-- Задание №2 -->
    <div class="task" id="task-2">
      <h3>Задание №2: Вывод текста при нажатии Ctrl и клике на ссылку</h3>
      <a href="#" @click.prevent="handleCtrlClick">Нажмите Ctrl + клик на меня</a>
      <p class="output">{{ ctrlOutput }}</p>
    </div>

    <!-- Задание №3 -->
    <div class="task" id="task-3">
      <h3>Задание №3: Вывод текста в зависимости от кнопки мыши</h3>
      <a href="#" @mousedown="handleMouseDown">Нажмите на меня</a>
      <p class="output">{{ mouseOutput }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      outputText: '',
      ctrlOutput: '',
      mouseOutput: '',
    };
  },
  methods: {
    showText() {
      this.outputText = this.inputText;
      this.inputText = ''; // Очистка инпута после ввода
    },
    handleCtrlClick(event) {
      if (event.ctrlKey) {
        this.ctrlOutput = 'Вы нажали Ctrl + клик!';
      }
    },
    handleMouseDown(event) {
      if (event.button === 0) {
        this.mouseOutput = 'left';
      } else if (event.button === 1) {
        this.mouseOutput = 'middle';
      } else if (event.button === 2) {
        this.mouseOutput = 'right';
      }
    },
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(247, 184, 214);
  border: 2px solidrgb(252, 112, 182);
  border-radius: 10px;
  padding: 20px;
  max-width: 500px;
  margin: auto;
}

.task {
  background-color:rgb(255, 211, 226);
  border: 1px solidrgb(247, 82, 165);
  border-radius: 5px;
  padding: 15px;
  margin-bottom: 20px;
}

h2 {
  text-align: center;
  color:rgb(193, 0, 96);
}

h3 {
  color: #cc0066;
}

input[type="text"] {
  width: calc(100% - 22px);
  padding: 10px;
  margin-top: 10px;
  border: 1px solidrgb(245, 68, 157);
  border-radius: 5px;
}

a {
  color:rgb(234, 15, 124);
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

.output {
  margin-top: 10px;
  font-weight: bold;
}
</style>