<script lang="ts">
import InfoSM from './components/InfoSM.vue';
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    InfoSM,
    Navbar
  },
  mounted() {
    this.initMouseLight();
  },
  methods: {
    initMouseLight() {
      const mouseLight = document.querySelector('.mouse-light') as HTMLElement;
      
      document.addEventListener('mousemove', (e) => {
        const x = e.clientX;
        const y = e.clientY;
        
        if (mouseLight) {
          mouseLight.style.left = x + 'px';
          mouseLight.style.top = y + 'px';
        }
      });
      
      document.addEventListener('mouseleave', () => {
        if (mouseLight) {
          mouseLight.style.opacity = '0';
        }
      });
      
      document.addEventListener('mouseenter', () => {
        if (mouseLight) {
          mouseLight.style.opacity = '0.4';
        }
      });
    }
  }
}
</script>

<template>
  <div class="app-container">
    <div class="mouse-light"></div>
    <Navbar />
    <InfoSM />
  </div>
</template>

<style scoped>
.app-container {
  position: relative;
  min-height: 100vh;
  overflow: hidden;
}

.mouse-light {
  position: fixed;
  width: 600px;
  height: 600px;
  border-radius: 50%;
  background: radial-gradient(
    circle,
    rgba(0, 123, 255, 0.15) 0%,
    rgba(0, 212, 255, 0.1) 25%,
    rgba(0, 123, 255, 0.05) 50%,
    transparent 70%
  );
  pointer-events: none;
  transform: translate(-50%, -50%);
  transition: opacity 0.3s ease;
  z-index: 9999;
  mix-blend-mode: screen;
  filter: blur(1px);
}

/* Efeito adicional para telas maiores */
@media (min-width: 1200px) {
  .mouse-light {
    width: 800px;
    height: 800px;
  }
}

/* Reduzir o efeito em telas menores */
@media (max-width: 768px) {
  .mouse-light {
    width: 400px;
    height: 400px;
    background: radial-gradient(
      circle,
      rgba(0, 123, 255, 0.1) 0%,
      rgba(0, 212, 255, 0.05) 25%,
      transparent 50%
    );
  }
}
</style>
