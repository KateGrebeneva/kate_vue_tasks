<template>
  <p v-if="!hidden">text</p>
</template>

<script>
export default {
  data() {
    return {
      hidden: true // Начальное значение для hidden
    };
  }
};
</script>

<style scoped>
p {
  color: #d5006d; /* Темно-розовый цвет текста */
  font-size: 20px; /* Размер шрифта */
  font-weight: bold; /* Жирный шрифт */
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5); /* Тень текста */
}
</style>

