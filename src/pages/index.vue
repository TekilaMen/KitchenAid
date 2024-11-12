<template>
  <div class="spline-background">
    <Navbar @change-component="changeComponent" />
    <spline-viewer loading-anim-type="spinner-small-dark" url="https://prod.spline.design/rRgk6Fdd5Vlp3JcE/scene.splinecode" />
    <Home v-if="activeComponent === 'home'" />
    <About v-if="activeComponent === 'about'" />
    <Services v-if="activeComponent === 'services'" />
    <Join v-if="activeComponent === 'join'" />
  </div>
</template>

<script lang="ts" setup>
  import { onMounted, ref } from 'vue'

  // Load Spline viewer properly
  const SPLINE_URL = 'https://unpkg.com/@splinetool/viewer@1.9.37/build/spline-viewer.js'

  onMounted(async () => {
    if (!customElements.get('spline-viewer')) {
      await import(SPLINE_URL)
    }
  })

  const activeComponent = ref('home')

  function changeComponent (component: string) {
    activeComponent.value = component
  }
</script>

<style>
/* Remove scoped to apply globally */
body {
  margin: 0;
  padding: 0;
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
  z-index: 1;
}

.spline-background spline-viewer {
  width: 100%;
  height: 100%;
  z-index: 1;
}

/* Add styles for components on top of Spline */
.home-container, .about-container {
  position: relative;
  z-index: 2;
}
</style>
