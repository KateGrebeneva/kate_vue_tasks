<template>
  <div class="container">
    <p :class="cssClasses">
      Семья — это всё. Утратить надежду обзавестись ею — величайшее из несчастий.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cssClasses: {
        active: true,
        valid: false
      }
    };
  }
};
</script>

<style scoped>
.container {
  background-color:rgb(255, 207, 247);
  padding: 20px;
  border-radius: 10px;
  text-align: center;
}

p {
  font-size: 20px;
  color: #333;
  padding: 10px;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.active {
  color: #ff0066;
  font-weight: bold;
}

.valid {
  background-color: #90ee90;
  color: #004d00;
}

.has-error {
  background-color: #ffcccc;
  color: #990000;
}

p.active {
  text-transform: uppercase;
}

p.valid {
  font-style: italic;
}
</style>