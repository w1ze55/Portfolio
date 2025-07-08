<script lang="ts">
import ProfileInfo from './ProfileInfo.vue'
import AboutMe from './AboutMe.vue'

export default {
    name: 'InfoSM',
    components: {
        ProfileInfo,
        AboutMe
    }
}
</script>

<template>
  <div class="portfolio-container">
      <div class="main-content">
          <ProfileInfo />
          <AboutMe />
      </div>
  </div>
</template>

<style scoped>
.portfolio-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.main-content {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 10rem;
  margin-bottom: 4rem;
}

/* Responsividade */
@media (max-width: 768px) {
  .main-content {
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 2rem;
  }
}

@media (max-width: 480px) {
  .portfolio-container {
      padding: 1rem;
  }
}
</style>
