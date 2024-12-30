<template>
  <section class="hero">
    <div class="image-background">
      <div class="image-overlay"></div>
      <img 
      :src="require('@/assets/images/DVEGEF_frontpage.png')" 
        alt="DVEGEF_frontpage"
        class="background-image"
      />
    </div>
    <div class="container hero-content">
     
    </div>
    <div class="scroll-indicator">
      <div class="mouse"></div>
      <span>Scroll to explore</span>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero {
  height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.image-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.background-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  transition: transform 0.8s ease;
}

/* .hero:hover .background-image {
  transform: scale(1.05);
} */

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background: linear-gradient(
    to bottom,
    rgba(10, 10, 10, 0.7) 0%,
    rgba(10, 10, 10, 0.5) 50%,
    rgba(10, 10, 10, 0.7) 100%
  ); */
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
  margin: 0 auto;
  padding: 0 2rem;
}

.glass-card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border-radius: 24px;
  padding: 3rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
  animation: fadeIn 1s ease-out;
}

.title {
  font-size: 4.5rem;
  margin-bottom: 1rem;
  font-weight: 700;
  line-height: 1.2;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.highlight {
  background: linear-gradient(90deg, var(--accent), #00C6FF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subtitle-text {
  font-size: 2rem;
  font-weight: 300;
  color: var(--text-secondary);
}

.subtitle {
  font-size: 1.5rem;
  color: var(--text-secondary);
  margin-bottom: 2.5rem;
  line-height: 1.6;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
}

.btn {
  padding: 1rem 2rem;
  border-radius: 12px;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 1.1rem;
}

.btn.primary {
  background: var(--accent);
  color: var(--text);
  box-shadow: 0 4px 15px rgba(0, 122, 255, 0.3);
}

.btn.secondary {
  background: rgba(255, 255, 255, 0.1);
  color: var(--text);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

/* .btn:hover {
  transform: translateY(-2px);
} */

.scroll-indicator {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  opacity: 0.7;
  animation: fadeInUp 1s ease-out 1s both;
  z-index: 2;
}

.mouse {
  width: 30px;
  height: 50px;
  border: 2px solid var(--text);
  border-radius: 20px;
  position: relative;
}

.mouse::before {
  content: '';
  width: 4px;
  height: 8px;
  background: var(--text);
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  top: 8px;
  border-radius: 2px;
  animation: scroll 1.5s infinite;
}

@keyframes scroll {
  0% { transform: translateX(-50%) translateY(0); opacity: 1; }
  100% { transform: translateX(-50%) translateY(20px); opacity: 0; }
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translate(-50%, 20px); }
  to { opacity: 0.7; transform: translate(-50%, 0); }
}

@media (max-width: 768px) {
  .title {
    font-size: 3rem;
  }
  
  .subtitle-text {
    font-size: 1.5rem;
  }
  
  .glass-card {
    padding: 2rem;
    margin: 1rem;
  }
  
  .cta-buttons {
    flex-direction: column;
  }
}
</style> 