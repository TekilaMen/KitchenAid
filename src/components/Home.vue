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
  padding: 20px 40px;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 10px;
  color: #ffffff;
  font-size: 64px;
  text-align: center;
  backdrop-filter: blur(2px);
}

.slogan {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #ffffff;
  font-size: 24px;
  text-align: center;
  font-family: 'Roboto', sans-serif;
}
</style>
