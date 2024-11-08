<template>
  <div class="card">
    Join Us
  </div>
  <div class="card description">
    Become a part of our culinary community and enhance your cooking skills.
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Join',
  })
</script>

<style scoped>
.card {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 30px 60px;
  background: rgba(0, 0, 0, 0.7); /* Darker background */
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  color: #ffffff;
  font-size: 24px;
  text-align: center;
  backdrop-filter: blur(5px);
}

.card.description {
  top: 60%;
  font-size: 16px;
  width: 80%;
}
</style>
