<template>
<div>
    <h1>Películas populares</h1>
    <ul v-if="movies.length">
    <li v-for="movie in movies" :key="movie.id">
        <img :src="getImageUrl(movie.poster_path)" alt="Poster" />
        {{ movie.title }} - {{ movie.release_date }}
    </li>
    </ul>
    <p v-else>Cargando películas...</p>
</div>
</template>

<script>
import axios from 'axios';

export default {
data() {
    return {
    movies: []
    };
},
created() {
    this.fetchPopularMovies();
},
methods: {
    async fetchPopularMovies() {
    const API_KEY = 'f7f892e15c090fb406936b0baff5ff78'; // Asegúrate de tener tu API_KEY en el archivo .env
    const BASE_URL = 'https://api.themoviedb.org/3';

    try {
        const response = await axios.get(`${BASE_URL}/movie/popular?api_key=${API_KEY}`);
        this.movies = response.data.results;
    } catch (error) {
        console.error("Error al obtener las películas:", error);
    }
    },
    getImageUrl(path) {
    return `https://image.tmdb.org/t/p/w500${path}`;
    }
}
};
</script>

