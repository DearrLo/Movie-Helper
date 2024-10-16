<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Bienvenue dans Movie Helper v1.1</h1>
    <!-- Intégration des émotions -->
    <Emotions />
  </div>
</template>

<script>
import Emotions from './components/EmotionsSelector.vue';

export default {
  name: 'App',
  components: {
    Emotions
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  margin-bottom: 20px;
}
</style>
