<template>
  <nav class="navbar">
    <ul>
      <li><a href="#home" @click.prevent="$emit('changeComponent', 'home')">Home</a></li>
      <li><a href="#about" @click.prevent="$emit('changeComponent', 'about')">About Us</a></li>
      <li><a href="#services" @click.prevent="$emit('changeComponent', 'services')">Services</a></li>
      <li><a href="#join" @click.prevent="$emit('changeComponent', 'join')">Join Us</a></li>
    </ul>
  </nav>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Navbar',
    emits: ['changeComponent'],
  })
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.1); /* Fond transparent */
  backdrop-filter: blur(5px);
  padding: 10px 20px;
  z-index: 1000;
  transition: background 0.3s ease;
}

.navbar ul {
  list-style: none;
  display: flex;
  justify-content: space-around;
  margin: 0;
  padding: 0;
}

.navbar ul li {
  margin: 0;
}

.navbar ul li a {
  color: #ffffff;
  text-decoration: none;
  font-size: 18px;
  font-family: 'Roboto', sans-serif;
  padding: 5px 10px;
  border-radius: 5px;
  transition: background 0.3s ease, color 0.3s ease;
}

.navbar ul li a:hover {
  background: rgba(255, 255, 255, 0.2); /* Fond légèrement plus opaque au survol */
  color: #000000; /* Couleur du texte au survol */
}
</style>
