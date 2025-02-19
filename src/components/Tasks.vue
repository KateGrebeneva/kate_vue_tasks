<template>
  <div class="container">
    <h2 class="title">Фильм "Собачья жизнь"</h2>
    <p :class="cssClasses">До безумства трогательный фильм, который рассказывает историю о верности и дружбе между человеком и собакой.</p>
  </div>
</template>

<script>
export default {
  name: 'DogLifeMovie',
  data() {
    return {
      cssClasses: 'highlighted bold', 
    };
  },
};
</script>

<style scoped>
.container {
  background-color:rgb(242, 121, 183); 
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  margin: 20px;
}

.title {
  color:rgb(182, 0, 94); 
  text-align: center;
  font-size: 2 em;
  margin-bottom: 15px;
}

p {
  font-size: 1.2em;
  text-align: center;
}

.highlighted {
  color:rgb(210, 14, 79); 
  background-color: rgba(255, 255, 255, 0.2); 
  padding: 10px;
  border-radius: 5px;
  transition: transform 0.3s; 
}

.bold {
  font-weight: bold; 
}

/* Эффект при наведении */
.highlighted:hover {
  transform: scale(1.05); 
}
</style>