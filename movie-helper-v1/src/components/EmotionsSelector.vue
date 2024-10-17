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

    <div v-if="movies.length">
      <h2>Films proposés :</h2>
      <ul>
        <li v-for="movie in movies" :key="movie.id">{{ movie.title }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      movies: [] // Liste des films récupérés
    };
  },
  methods: {
    selectEmotion(emotion) {
      console.log(`Emotion selected: ${emotion}`);
      this.fetchMovies(emotion); // Appelle la fonction pour récupérer les films
    },

    async fetchMovies(emotion) {
      if (emotion === 'Goofy') {
        try {
          const response = await axios.get(
            'https://api.themoviedb.org/3/discover/movie',
            {
              params: {
                api_key: process.env.VUE_APP_TMDB_API_KEY,
                with_genres: '35' // Genre comédie
              }
            }
          );
          this.movies = response.data.results;
          console.log(this.movies); // Pour voir les films dans la console
        } catch (error) {
          console.error('Erreur lors de la récupération des films :', error);
          console.log('Détails de l\'erreur :', error.response); // Affiche plus d'infos sur l'erreur
        }
      }
    }
  }
};
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
  background-color: transparent; 
  cursor: pointer;
}

button img {
  width: 50px; /* Taille de l'icône */
  height: 50px;
  transition: transform 0.3s ease; /* Ajout de la transition douce */
}

button img:hover {
  transform: scale(1.4); /* Agrandit l'icône lors du survol */
}
</style>