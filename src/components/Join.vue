<template>
  <div class="card title">
    Join Us
    <div class="underline" />
  </div>
  <div class="stats-container">
    <div class="stat-card">
      <span class="stat-number">10K+</span>
      <span class="stat-label">Active Members</span>
    </div>
    <div class="stat-card">
      <span class="stat-number">5K+</span>
      <span class="stat-label">Recipes Shared</span>
    </div>
    <div class="stat-card">
      <span class="stat-number">24/7</span>
      <span class="stat-label">Community Support</span>
    </div>
  </div>
  <div class="join-options">
    <div class="join-card">
      <div class="icon-wrapper">
        <i class="fab fa-discord" />
      </div>
      <h3>Join our Discord</h3>
      <p>Connect with our community, share recipes, and get instant support.</p>
      <div class="card-footer">
        <v-btn
          class="join-button discord"
          href="https://discord.gg/ku45sj4edT"
          rel="noopener noreferrer"
          target="_blank"
          variant="flat"
        >
          <div class="button-content">
            <i class="fab fa-discord mr-2" />
            <span>Join Discord</span>
          </div>
        </v-btn>
      </div>
    </div>
    <div class="join-card">
      <div class="icon-wrapper">
        <i class="fas fa-envelope" />
      </div>
      <h3>Contact by Email</h3>
      <p>Get in touch with our team directly for professional inquiries.</p>
      <div class="card-footer">
        <v-btn
          class="join-button email"
          variant="flat"
          @click="copyEmail"
        >
          <div class="button-content">
            <i class="fas fa-envelope mr-2" />
            <span>Send Email</span>
          </div>
        </v-btn>
      </div>
    </div>
  </div>

  <v-snackbar
    v-model="snackbar"
    class="custom-snackbar"
    color="success"
    location="top"
    rounded="pill"
    :timeout="2000"
  >
    <div class="snackbar-content">
      <v-icon class="mr-2" icon="mdi-check-circle" />
      <span>Email copied to clipboard!</span>
    </div>
  </v-snackbar>
</template>

<script lang="ts">
  import { defineComponent, ref } from 'vue'

  export default defineComponent({
    name: 'Join',
    setup () {
      const snackbar = ref(false)

      const copyEmail = () => {
        navigator.clipboard.writeText('kitchen.aid.ai@gmail.com')
        snackbar.value = true
      }

      return {
        snackbar,
        copyEmail,
      }
    },
  })
</script>

<style scoped>
.card.title {
  position: absolute;
  top: 15%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 20px 40px;
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  color: #ffffff;
  font-size: 28px;
  text-align: center;
  backdrop-filter: blur(5px);
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 500;
  letter-spacing: 0.5px;
  position: relative;
}

.underline {
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 50px;
  height: 3px;
  background: linear-gradient(90deg, #ff6b6b, #4ecdc4);
  border-radius: 2px;
}

.stats-container {
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  gap: 2rem;
  width: 80%;
  max-width: 800px;
  justify-content: center;
}

.stat-card {
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  padding: 20px;
  color: #ffffff;
  text-align: center;
  backdrop-filter: blur(5px);
  transition: all 0.3s ease;
  min-width: 150px;
}

.stat-card:hover {
  transform: translateY(-5px);
  border-color: #4ecdc4;
}

.stat-number {
  display: block;
  font-family: 'Space Grotesk', sans-serif;
  font-size: 28px;
  font-weight: 600;
  color: #4ecdc4;
  margin-bottom: 5px;
}

.stat-label {
  display: block;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  opacity: 0.9;
}

.join-options {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  gap: 2rem;
  width: 80%;
  max-width: 1000px;
  justify-content: center;
}

.join-card {
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  padding: 30px;
  color: #ffffff;
  text-align: center;
  backdrop-filter: blur(5px);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  flex: 1;
  max-width: 400px;
  position: relative;
  overflow: hidden;
}

.join-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, rgba(255,107,107,0.1), rgba(78,205,196,0.1));
  opacity: 0;
  transition: opacity 0.3s ease;
}

.join-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.3);
}

.join-card:hover::before {
  opacity: 1;
}

.icon-wrapper {
  width: 60px;
  height: 60px;
  margin: 0 auto 20px;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease;
}

.icon-wrapper i {
  font-size: 24px;
  color: #4ecdc4;
}

.join-card:hover .icon-wrapper {
  transform: rotate(360deg);
}

.join-card h3 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 20px;
  margin-bottom: 15px;
  letter-spacing: 0.3px;
}

.join-card p {
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  margin-bottom: 25px;
  line-height: 1.6;
  letter-spacing: 0.2px;
}

.join-button {
  padding: 12px 30px !important;
  border-radius: 25px !important;
  color: white !important;
  font-family: 'Poppins', sans-serif !important;
  font-size: 14px !important;
  width: 100% !important;
  text-transform: none !important;
  height: 48px !important;
  display: flex !important;
  align-items: center !important;
  justify-content: center !important;
}

.button-content {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  gap: 8px;
}

.join-button.discord {
  background-color: #7289da !important;
}

.join-button.email {
  background-color: #4ecdc4 !important;
}

.join-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.3) !important;
}

:deep(.custom-snackbar) {
  font-family: 'Poppins', sans-serif !important;
}

:deep(.v-snackbar__wrapper) {
  color: white !important;
}

:deep(.v-snackbar__content) {
  padding: 12px 24px !important;
  font-size: 14px !important;
  letter-spacing: 0.2px !important;
}

.snackbar-content {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

@media (max-width: 768px) {
  .stats-container {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    top: 35%;
  }

  .stat-card {
    width: 100%;
    max-width: 200px;
  }

  .join-options {
    flex-direction: column;
    align-items: center;
    top: 70%;
  }

  .join-card {
    width: 100%;
  }
}
</style>
