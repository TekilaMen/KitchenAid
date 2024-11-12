<template>
  <div class="card">
    DevBro's
  </div>
  <div class="team-container">
    <div class="member-card">
      <img alt="Léo STEPHAN" src="/leo.jpg">
      <h3>Léo STEPHAN</h3>
      <p>Ingénieur Front-end</p>
    </div>
    <div class="member-card">
      <img alt="Sammuel LEROUX" src="/sam.jpg">
      <h3>Sammuel LEROUX</h3>
      <p>Ingénieur DevOps</p>
    </div>
    <div class="member-card">
      <img alt="Théo GAGELIN" src="/theo.jpg">
      <h3>Théo GAGELIN</h3>
      <p>Ingénieur Back-end</p>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'About',
  })
</script>

<style scoped>
.card {
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 30px 60px;
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  color: #ffffff;
  font-size: 24px;
  text-align: center;
  backdrop-filter: blur(5px);
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 500;
  letter-spacing: 0.5px;
}

.team-container {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  gap: 2rem;
  justify-content: center;
  width: 90%;
}

.member-card {
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  padding: 20px;
  color: #ffffff;
  text-align: center;
  backdrop-filter: blur(5px);
  font-family: 'Poppins', sans-serif;
}

.member-card img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 1rem;
}

.member-card h3 {
  margin: 0.5rem 0;
  font-size: 1.2rem;
  font-weight: 500;
  letter-spacing: 0.3px;
}

.member-card p {
  margin: 0;
  font-size: 1rem;
  font-weight: 300;
  letter-spacing: 0.2px;
  opacity: 0.9;
}
</style>
