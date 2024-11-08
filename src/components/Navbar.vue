<template>
  <nav class="navbar">
    <ul>
      <li><a @click.prevent="$emit('changeComponent', 'home')">Home</a></li>
      <li><a @click.prevent="$emit('changeComponent', 'about')">About Us</a></li>
      <li><a @click.prevent="$emit('changeComponent', 'services')">Services</a></li>
      <li><a @click.prevent="$emit('changeComponent', 'join')">Join Us</a></li>
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
  background: rgba(0, 0, 0, 0.8); /* Darker background */
  backdrop-filter: blur(10px);
  padding: 15px 30px;
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
  padding: 10px 20px;
  border-radius: 5px;
  transition: background 0.3s ease, color 0.3s ease;
}

.navbar ul li a:hover {
  background: rgba(255, 255, 255, 0.2); /* Slightly more opaque background on hover */
  color: #000000; /* Text color on hover */
}
</style>
