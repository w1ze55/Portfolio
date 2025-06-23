<script lang="ts">
export default {
    name: 'InfoSM',
    data() {
        return {
            name: 'Caue Peres',
            description: 'Welcome to my portfolio!',
            title: 'Developer FullStack Jr',
        }
    } 
}
</script>

<template>
  
  <div class="img-logo">
    <img src="../assets/foto eu.jpg" alt="Foto de perfil">
  </div>
    <div class="app">
        <header class="hero">
            <h1>{{ name }}</h1>
            <h2>{{ title }}</h2>
            <p>{{ description }}</p>
        </header>
    </div>
</template>

<style scoped>
img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}

.app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.hero {
  text-align: center;
  margin-bottom: 4rem;
}

.hero h1 {
  font-size: 3rem;
}

.hero h2 {
  font-size: 1.5rem;
}

section {
  margin-bottom: 3rem;
}

h3 {
  font-size: 2rem;
  border-bottom: 2px solid #3498db;
  padding-bottom: 0.5rem;
}
</style>