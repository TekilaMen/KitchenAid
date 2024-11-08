<template>
  <div class="spline-background">
    <Navbar @change-component="changeComponent" />
    <spline-viewer url="https://prod.spline.design/rRgk6Fdd5Vlp3JcE/scene.splinecode" />
    <Home v-if="activeComponent === 'home'" />
  </div>
</template>

<script lang="ts" setup>
  import { ref } from 'vue'
  import 'https://unpkg.com/@splinetool/viewer@1.9.37/build/spline-viewer.js'

  const activeComponent = ref('home')

  function changeComponent (component: string) {
    activeComponent.value = component
  }
</script>

<style scoped>
body {
  background-color: #000000;
  color: #ffffff;
  font-family: 'Cinzel', serif;
}

.spline-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.spline-background spline-viewer {
  width: 100%;
  height: 100%;
}
</style>
