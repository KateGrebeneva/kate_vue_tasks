<template>
  <div class="container">
    <button @click="toggleVisibility" class="toggle-button">
      {{ visible ? 'Скрыть текст' : 'Показать текст' }}
    </button>
    
    <p v-if="visible" class="text-visible">Первый абзац: текст виден!</p>
    <p v-else class="text-hidden">Второй абзац: текст скрыт!</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: true, // Начальное значение для видимости
    };
  },
  methods: {
    toggleVisibility() {
      this.visible = !this.visible; // Переключаем значение visible
    }
  }
};
</script>

<style scoped>
.container {
  text-align: center;
  padding: 50px;
  background-color:rgb(255, 207, 245); 
}

.toggle-button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: rgb(208, 47, 130); 
  color: white;
  font-size: 1em;
  cursor: pointer;
  transition: background-color 0.3s;
}

.toggle-button:hover {
  background-color: rgb(165, 38, 100); 
}

.text-visible {
  color: rgb(208, 47, 130); 
  font-size: 1.5em;
}

.text-hidden {
  color: rgba(208, 47, 130, 0.5); 
  font-size: 1.5em;
}
</style>
