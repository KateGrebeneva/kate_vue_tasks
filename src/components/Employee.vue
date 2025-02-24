<template>
  <div class="employee-card">
    <template v-if="!isEdit">
      <span class="employee-name">{{ name }} {{ surn }}</span>
      <button class="edit-button" @click="edit">Редактировать</button>
    </template>
    <template v-else>
      <input v-model="newName" class="input-field" placeholder="Имя" />
      <input v-model="newSurn" class="input-field" placeholder="Фамилия" />
      <button class="save-button" @click="save">Сохранить</button>
    </template>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const props = defineProps({
  id: Number,
  name: String,
  surn: String,
});

const emit = defineEmits(['change']);

const isEdit = ref(false);
const newName = ref(props.name);
const newSurn = ref(props.surn);

const edit = () => {
  isEdit.value = true;
};

const save = () => {
  isEdit.value = false;
  emit('change', props.id, newName.value, newSurn.value);
};
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

.edit-button,
.save-button {
  background-color: rgb(250, 62, 156); /* Розовая кнопка */
  color: white; /* Белый цвет текста */
  border: none; /* Без границ */
  border-radius: 5px; /* Скругленные углы */
  padding: 5px 10px; /* Внутренние отступы */
  cursor: pointer; /* Курсор в виде указателя */
}

.edit-button:hover,
.save-button:hover {
  background-color: rgba(250, 62, 156, 0.8); /* Темнее при наведении */
}

.input-field {
  margin-right: 10px; /* Отступ между инпутами и кнопкой */
  padding: 5px; /* Внутренние отступы */
  border: 1px solid rgb(250, 62, 156); /* Розовая рамка инпутов */
  border-radius: 5px; /* Скругленные углы */
}
</style>