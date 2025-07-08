<script lang="ts">
export default {
    name: 'ProfileInfo',
    data() {
        return {
            name: 'Caue Peres',
            description: 'Welcome to my portfolio!',
            title: 'Developer FullStack Jr'
        }
    } 
}
</script>

<template>
  <div class="profile-section">
      <header class="profile-header">
          <h1>{{ name }}</h1>
          <h2>{{ title }}</h2>
          <p class="welcome-message">{{ description }}</p>
      </header>
  </div>
</template>

<style scoped>
.profile-section {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.profile-header {
  margin-bottom: 2rem;
}

.profile-header h1 {
  font-size: 3rem;
  margin-bottom: 0.5rem;
  background: linear-gradient(135deg, #007bff, #00d4ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.profile-header h2 {
  font-size: 1.5rem;
  color: #007bff;
  margin-bottom: 1rem;
  font-weight: 400;
}

.welcome-message {
  font-size: 1.1rem;
  line-height: 1.6;
  opacity: 0.9;
}

/* Responsividade */
@media (max-width: 768px) {
  .profile-header h1 {
      font-size: 2.5rem;
  }
  
  .profile-header h2 {
      font-size: 1.3rem;
  }
}

@media (max-width: 480px) {
  .profile-header h1 {
      font-size: 2rem;
  }
  
  .profile-header h2 {
      font-size: 1.2rem;
  }
}
</style> 