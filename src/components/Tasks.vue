<template>
  <div class="container">
    <button @click="show" class="styled-button">Показать текст</button>
    <button @click="hide" class="styled-button">Скрыть текст</button>
    <p v-if="visible" class="styled-text">Это текст, который можно скрывать и показывать.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false, // Изначально текст скрыт
    };
  },
  methods: {
    hide() {
      this.visible = false; // Скрываем текст
    },
    show() {
      this.visible = true; // Показываем текст
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center; 
  margin-top: 50px; 
}

.styled-text {
  color: #d5006d; 
  font-size: 24px; 
  font-weight: bold;
  text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3); 
  transition: opacity 0.5s;
}

.styled-button {
  background-color: #d5006d; 
  color: white; 
  border: none; 
  border-radius: 8px; 
  padding: 12px 24px; 
  font-size: 18px; 
  cursor: pointer; 
  transition: background-color 0.3s, transform 0.2s; 
}

.styled-button:hover {
  background-color: #c51162; 
}

.styled-button:active {
  transform: scale(0.95); 
}
</style>