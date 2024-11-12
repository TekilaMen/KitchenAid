<template>
  <div class="card title">
    Our Services
    <div class="underline" />
  </div>
  <div class="services-grid">
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-utensils" />
      </div>
      <h3>Recipe Discovery</h3>
      <p>Discover recipes tailored to your tastes, dietary preferences, and goals. Get ingredient alternatives with AI-based suggestions.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-filter" />
      </div>
      <h3>Advanced Filters</h3>
      <p>Refine your recipe search by cuisine type, preparation time, dietary needs, and more.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-barcode" />
      </div>
      <h3>Scan & Enter Ingredients</h3>
      <p>Scan ingredients with image recognition to get recipe suggestions, or manually enter items you have.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-chart-pie" />
      </div>
      <h3>Nutrition Stats</h3>
      <p>Track your eating habits and analyze personalized nutrition stats to improve your health.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-gift" />
      </div>
      <h3>Loyalty & Rewards</h3>
      <p>Earn points as you use the app and receive rewards. Find partner stores to enjoy exclusive benefits.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
    <div class="service-card">
      <div class="icon-wrapper">
        <i class="fas fa-user-cog" />
      </div>
      <h3>Profile & Preferences</h3>
      <p>Set up your profile, save your preferences, and access your history to find favorite recipes easily.</p>
      <div class="card-footer">
        <button class="learn-more">Learn More</button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Services',
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

.services-grid {
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  width: 90%;
  max-width: 1200px;
  padding: 20px;
}

.service-card {
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 15px;
  padding: 20px;
  color: #ffffff;
  text-align: center;
  backdrop-filter: blur(5px);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.service-card::before {
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

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.3);
}

.service-card:hover::before {
  opacity: 1;
}

.icon-wrapper {
  width: 50px;
  height: 50px;
  margin: 0 auto 15px;
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

.service-card:hover .icon-wrapper {
  transform: rotate(360deg);
}

.service-card h3 {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 500;
  font-size: 18px;
  margin-bottom: 8px;
  letter-spacing: 0.3px;
}

.service-card p {
  font-family: 'Poppins', sans-serif;
  font-weight: 300;
  font-size: 13px;
  line-height: 1.4;
  letter-spacing: 0.2px;
}

.card-footer {
  margin-top: 15px;
}

.learn-more {
  background: transparent;
  border: 1px solid rgba(255,255,255,0.2);
  color: white;
  padding: 8px 20px;
  border-radius: 20px;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  cursor: pointer;
  transition: all 0.3s ease;
  opacity: 0;
  transform: translateY(20px);
}

.service-card:hover .learn-more {
  opacity: 1;
  transform: translateY(0);
}

.learn-more:hover {
  background: rgba(255,255,255,0.1);
  border-color: rgba(255,255,255,0.3);
}

@media (max-width: 1024px) {
  .services-grid {
    top: 60%;
    width: 95%;
    gap: 1rem;
  }
}

@media (max-width: 768px) {
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .services-grid {
    grid-template-columns: 1fr;
  }
}
</style>
