<script lang="ts">
export default {
    name: 'AboutMe',
    data() {
        return {
            aboutMe: 'colocar meu texto de apresentação'
        }
    } 
}
</script>

<template>
  <div class="info-section">
      <section class="about-card">
          <h3>About me</h3>
          <p class="about-description">{{ aboutMe }}</p>
      </section>
  </div>
</template>

<style scoped>
.info-section {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.about-card {
  background: rgba(255, 255, 255, 0.1) !important;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 
      0 8px 32px rgba(0, 123, 255, 0.1),
      inset 0 1px 0 rgba(255, 255, 255, 0.2);
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
}

.about-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(0, 123, 255, 0.8), transparent);
  animation: shimmer 3s infinite;
}

.about-card:hover {
  transform: translateY(-5px);
  box-shadow: 
      0 15px 40px rgba(0, 123, 255, 0.2),
      inset 0 1px 0 rgba(255, 255, 255, 0.3);
  border-color: rgba(0, 123, 255, 0.3);
}

.about-card h3 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: #00d4ff;
  text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
  position: relative;
  background: transparent !important;
}

.about-card h3::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 0;
  width: 60px;
  height: 3px;
  background: linear-gradient(90deg, #007bff, #00d4ff) !important;
  border-radius: 2px;
  box-shadow: 0 0 10px rgba(0, 123, 255, 0.5);
}

.about-description {
  font-size: 1.1rem;
  line-height: 1.8;
  text-align: justify;
  color: rgba(255, 255, 255, 0.9);
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
  background: transparent !important;
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

/* Responsividade */
@media (max-width: 768px) {
  .about-description {
      text-align: left;
  }
}
</style> 