<template>
  <div id="app">
    <header class="app-header">
      <Button type="primary" class="yellow-button">IMDb</Button>
      <Navbar />
      <SettingsButton />
      <Avatar imageUrl="https://i.pinimg.com/564x/56/5c/34/565c34434a73fbfb77e72aaebb986ef4.jpg" />
    </header>
    
    <MovieList />
    
    <Card
      :image="'ruta/a/tu/imagen.jpg'"
      title="Título de la Tarjeta"
      description="Esta es una descripción para la tarjeta"
    >
      <Button type="primary" @click="handleButtonClick">Haz clic en mí</Button>
    </Card>
  </div>
</template>



<script lang="ts">
import { defineComponent } from 'vue';
import MovieList from './components/Movie_list.vue';
import Card from './components/common/Card.vue';
import Button from './components/common/Button.vue';
import Navbar from './components/common/Navbar.vue';
import SettingsButton from './components/common/SettingsButton.vue';  // Asumiendo que tienes un componente para esto
import Avatar from './components/common/Avatar.vue';  // Asumiendo que tienes un componente para esto
import './assets/styles/variables.css'


export default defineComponent({
  name: 'App',
  components: {
    Card,
    Button,
    MovieList,
    Navbar,
    SettingsButton,  // Si tienes este componente
    Avatar  // Si tienes este componente
  },
  methods: {
    handleButtonClick() {
      alert('¡Botón presionado!');
    }
  }
});
</script>

<style scoped>
/* Ajustes de estilos */
.top-left-button {
  position: absolute;
  top: 10px;
  left: 10px;
}
/* Puedes añadir más estilos según lo necesites */
</style>
