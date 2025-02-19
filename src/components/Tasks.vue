<template>
  <div class="product-list-container">
    <h1 class="title">Список продуктов</h1>
    <ul class="product-list">
      <li v-for="product in products" :key="product.id" class="product-item">
        {{ product.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ProductList',
  data() {
    return {
      products: [
        { id: 1, name: 'Regina' },
        { id: 2, name: 'Emma' },
        { id: 3, name: 'Belle' },
      ],
    };
  },
};
</script>

<style scoped>
.product-list-container {
  background-color:rgb(251, 193, 227); 
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.title {
  color: #d5006d; 
  text-align: center;
  font-family: 'Arial', sans-serif; 
  margin-bottom: 20px;
}

.product-list {
  list-style-type: none; 
  padding: 0; 
}

.product-item {
  color: #d5006d; 
  font-size: 18px;
  margin: 10px 0; 
  padding: 10px; 
  border: 2px solid #d5006d; 
  border-radius: 10px;
  transition: background-color 0.3s, transform 0.2s; 
}

.product-item:hover {
  background-color:rgb(250, 194, 213); 
  transform: scale(1.05);
}
</style>