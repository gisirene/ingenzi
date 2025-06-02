<script setup>
import gaming from './components/gamelist.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <gaming msg="You did it!" />
    </div>
  </header>

  <main>
  
  </main>
</template>

<style scoped>
.app {
  max-width: 400px;
  margin: auto;
  text-align: center;
  padding: 20px;
  font-family: Arial;
}

input {
  padding: 8px;
  margin-right: 10px;
  width: 60%;
}

button {
  padding: 8px 12px;
}

ul {
  margin-top: 20px;
  text-align: left;
}
</style>
