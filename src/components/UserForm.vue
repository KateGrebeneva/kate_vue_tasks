<template>
  <div class="form-container">
    <input v-model="newName" class="input-field" placeholder="Имя" />
    <input v-model="newSurn" class="input-field" placeholder="Фамилия" />
    <button @click="save" class="submit-button">Сохранить</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const emit = defineEmits(['add']);

const newName = ref('');
const newSurn = ref('');

const save = () => {
  if (newName.value && newSurn.value) {
    emit('add', newName.value, newSurn.value);
    newName.value = '';
    newSurn.value = '';
  } else {
    alert('Пожалуйста, заполните все поля!');
  }
};
</script>

<style scoped>
.form-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 20px;
}

.input-field {
  padding: 10px;
  margin: 5px;
  border: 2px solid rgb(250, 62, 156); /* Розовая рамка */
  border-radius: 5px; /* Скругленные углы */
  width: 200px; /* Ширина инпутов */
}

.submit-button {
  background-color: rgb(250, 62, 156); /* Розовая кнопка */
  color: white; /* Белый цвет текста */
  border: none; /* Без границ */
  border-radius: 5px; /* Скругленные углы */
  padding: 10px; /* Внутренние отступы */
  cursor: pointer; /* Курсор в виде указателя */
}

.submit-button:hover {
  background-color: rgba(250, 62, 156, 0.8); /* Темнее при наведении */
}
</style>