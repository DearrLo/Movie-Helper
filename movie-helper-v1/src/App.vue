<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>𝐖𝐞𝐥𝐜𝐨𝐦𝐞 𝐭𝐨 𝐌𝐎𝐕𝐈𝐄 𝐇𝐄𝐋𝐏𝐄𝐑</h1>
    <h3>𝐩𝐥𝐞𝐚𝐬𝐞, 𝐩𝐢𝐜𝐤 𝐚𝐧 𝐞𝐦𝐨𝐭𝐢𝐨𝐧 𝐛𝐞𝐥𝐨𝐰 𝐚𝐧𝐝 𝐥𝐞𝐭 𝐨𝐮𝐫 𝐚𝐩𝐩 𝐩𝐢𝐜𝐤𝐢𝐧𝐠 𝐭𝐡𝐞 𝐛𝐞𝐬𝐭 𝐜𝐡𝐨𝐢𝐜𝐞𝐬 𝐟𝐨𝐫 𝐲𝐨𝐮.</h3>
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

body {
  background-color: #E8D5CC; 
  margin: 0;
  padding: 0;
  min-height: 100vh; 
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #37040E;
  margin-top: 60px;
}

h1 {
  margin-bottom: 20px;
}
</style>
