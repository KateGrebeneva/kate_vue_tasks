<template>
  <div class="container">
    <p v-if="age < 18" class="text">Подросток</p>
    <p v-else-if="age >= 18 && age <= 25" class="text">Девушка</p>
    <p v-else class="text">Женщина</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: 18, 
    };
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
  font-size: 24px;
  background-color: #ff69b4; 
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
}

.text {
  color: white;
  font-weight: bold; 
}
</style>
