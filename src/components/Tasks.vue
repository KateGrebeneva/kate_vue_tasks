<template>
  <div>
    <div class="user-name">{{ name }}</div>
    <div class="user-surname">{{ surn }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Emma',
      surn: 'Swan',
    }
  }
}
</script>

<style scoped>
.user-name, .user-surname {
  color: #D5006D; /* Темно-розовый цвет */
  font-family: 'Arial', sans-serif; /* Шрифт */
  font-size: 20px; /* Размер шрифта */
  margin: 10px 0; /* Отступы */
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3); /* Тень текста */
}
</style>