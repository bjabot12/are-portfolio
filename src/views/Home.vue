<template>
  <div class="home">
    <section class="hero">
      <div class="hero-content">
        <Hero />
      </div>
    </section>
    <Projects />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
import Projects from '@/components/Projects.vue'

export default {
  name: 'HomePage',
  components: {
    Hero,
    Projects
  },
  data() {
    return {
      showScrollIndicator: true
    }
  },
  created() {
    this.showScrollIndicator = true
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.showScrollIndicator = window.pageYOffset < 10
    }
  }
}
</script>

<style scoped>
.home {
  position: relative;
  height: 100%;
}

.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-bottom: 4rem;
}

.hero-content {
  flex: 1;
  /* ... other existing hero-content styles ... */
}

.scroll-indicator {
  position: absolute;
  /* bottom: 100%; */
  padding-top: 53rem;
  left: 50%;
  transform: translateX(-50%);
  z-index: 999;
}

.arrow {
  color: white;
  font-size: 2rem;
  opacity: 0.7;
  animation: bounce 2s infinite;
  font-family: Arial, sans-serif;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
}

@media (max-width: 768px) {
  .hero {
    padding-bottom: 3rem;
  }

  .scroll-indicator {
    /* bottom: 1.5rem; */
  }
  
  .arrow {
    font-size: 1.5rem;
  }
}
@media (max-width: 480px) {
  .project-title {
    font-size: 1rem;
  }
  .hero {
    padding-bottom: 3rem;
  }

  .scroll-indicator {
    /* bottom: 1.5rem; */
  }
  
  .arrow {
    font-size: 1.5rem;
  }
}
</style> 