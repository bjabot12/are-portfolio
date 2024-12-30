<template>
  <div id="app">
    <NavBar />
    <Hero />
    <Projects />
    <About />
    <Contact />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Hero from './components/Hero.vue'
import Projects from './components/Projects.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Hero,
    Projects,
    About,
    Contact
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

#app {
  font-family: 'Poppins', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
