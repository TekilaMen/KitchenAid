<template>
  <div class="card">
    Kitchen Aid
  </div>
  <div class="slogan">
    "Empowering Your Culinary Journey"
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Home',
  })
</script>

<style scoped>
.card {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 30px 60px;
  background: rgba(0, 0, 0, 0.7); /* Darker background */
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  color: #ffffff;
  font-size: 64px;
  text-align: center;
  backdrop-filter: blur(5px);
}

.slogan {
  position: absolute;
  top: 65%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #ffffff;
  font-size: 24px;
  text-align: center;
  font-family: 'Roboto', sans-serif;
}
</style>
