<template>
  <div class="container">
    <div v-for="(item, index) in items" :key="index" class="item">
      <button @click="toggle(index)" class="styled-button">
        {{ item.visible ? 'Скрыть' : 'Показать' }} {{ item.title }}
      </button>
      <p v-if="item.visible" class="styled-text">{{ item.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'Принцесса Ариэль', text: 'Ариэль — русалочка, которая мечтает стать человеком.', visible: false },
        { title: 'Принцесса Белль', text: 'Белль — умная и независимая девушка, которая любит читать книги.', visible: false },
        { title: 'Принцесса Жасмин', text: 'Жасмин — смелая принцесса, которая стремится к свободе и приключениям.', visible: false },
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