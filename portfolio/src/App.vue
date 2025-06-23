<script lang="ts">
import InfoSM from './components/InfoSM.vue';
import Navbar from './components/Navbar.vue';
export default {
  name: 'App',
  components: {
    InfoSM,
    Navbar
  }
}
</script>

<template>
  <Navbar />
  <InfoSM />
</template>

<style scoped>

</style>
