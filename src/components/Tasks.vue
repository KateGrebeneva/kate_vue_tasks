<template>
  <div class="link-container">
    <a :href="href" class="styled-link">{{ text }}</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Adventures of the Gummi Bears',
      href: 'https://www.kinopoisk.ru/series/81023/',
    }
  }
}
</script>

<style scoped>
.link-container {
  display: flex; 
  justify-content: center; 
  margin-top: 20px; 
}

.styled-link {
  color: #D5006D;
  font-family: 'Arial', sans-serif; 
  font-size: 24px;
  text-decoration: none; 
  transition: color 0.3s ease; 
}

.styled-link:hover {
  color: #FF4081; 
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}
</style>
