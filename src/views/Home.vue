<template>
  <div class="home">
    <Hero />
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
  }
}
</script> 