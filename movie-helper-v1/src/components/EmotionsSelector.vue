<template>
  <div class="emotions">
    <button @click="selectEmotion('Goofy')">
      <img src="@/assets/goofy.png" alt="Goofy" />
    </button>
    <button @click="selectEmotion('Depressed')">
      <img src="@/assets/depressed.png" alt="Depressed" />
    </button>
    <button @click="selectEmotion('Flirty')">
      <img src="@/assets/flirty.png" alt="Flirty" />
    </button>
    <button @click="selectEmotion('Phenomenal')">
      <img src="@/assets/phenomenal.png" alt="Phenomenal" />
    </button>
    <button @click="selectEmotion('Spooky')">
      <img src="@/assets/spooky.png" alt="Spooky" />
    </button>
  </div>
</template>

<script>
export default {
  name: 'EmotionsSelector', // Nom à plusieurs mots pour éviter les erreurs ESLint
  methods: {
    selectEmotion(emotion) {
      console.log('Emotion selected:', emotion);
      // Ici tu peux gérer la sélection de l'émotion
    }
  }
}
</script>

<style scoped>
.emotions {
  text-align: center;
  margin-top: 20px;
}

button {
  margin: 10px;
  padding: 10px;
  border: none;
  background-color: transparent; /* Retire le fond du bouton */
  cursor: pointer;
}

button img {
  width: 50px; /* Taille de l'image */
  height: 50px;
}
</style>
