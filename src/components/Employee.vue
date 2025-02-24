<template>
  <div class="employee-card">
    <span class="employee-name">{{ name }} {{ surn }}</span>
    <button class="remove-button" @click="$emit('remove', id)">
      Удалить
    </button>
  </div>
</template>

<script setup>
defineProps({
  id: Number,
  name: String,
  surn: String,
});

defineEmits(['remove']);
</script>

<style scoped>
.employee-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  margin-bottom: 10px;
  background-color: #fff; /* Белый фон карточки */
  border: 2px solid rgb(250, 62, 156); /* Розовая рамка */
  border-radius: 8px; /* Скругленные углы */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Тень */
}

.employee-name {
  color: rgb(250, 62, 156); /* Розовый цвет текста */
}

.remove-button {
  background-color: rgb(250, 62, 156); /* Розовая кнопка */
  color: white; /* Белый цвет текста */
  border: none; /* Без границ */
  border-radius: 5px; /* Скругленные углы */
  padding: 5px 10px; /* Внутренние отступы */
  cursor: pointer; /* Курсор в виде указателя */
}

.remove-button:hover {
  background-color: rgba(250, 62, 156, 0.8); /* Темнее при наведении */
}
</style>