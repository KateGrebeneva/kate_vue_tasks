<template>
  <div class="container">
    <div v-for="(item, index) in items" :key="index" class="item">
      <button @click="toggle(index)" class="styled-button">Toggle Paragraph {{ index + 1 }}</button>
      <p v-if="item.visible" class="styled-text">{{ item.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { text: 'Румпельштильцхен — Тёмный, сильнейший из волшебников Зачарованного Леса.', visible: false },
        { text: 'Очень хитрый и проницательный, загадочный и увёртливый маг.', visible: false },
        { text: 'Является учителем трёх великих колдуний семейства Миллс — Коры, Реджины и Зелины.', visible: false },
      ],
    };
  },
  methods: {
    toggle(index) {
      this.items[index].visible = !this.items[index].visible; // Инвертируем видимость
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center; 
  margin-top: 50px; 
}

.item {
  margin-bottom: 20px; 
}

.styled-text {
  color: #d5006d; 
  font-size: 20px; 
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