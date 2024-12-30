<template>
    <nav class="navbar">
      <div class="container nav-container">
        <a href="/" class="logo">Are Botnevik</a>
        <div class="nav-links">
          <a href="#work" @click.prevent="scrollToSection('work')"><b>WORK</b></a>
          <router-link to="/about"><b>ABOUT</b></router-link>
          <router-link to="/contact"><b>CONTACT</b></router-link>
        </div>
      </div>
    </nav>
  </template>

<script>
export default {
  name: 'NavBar',
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId)
      if (element) {
        element.scrollIntoView({ 
          behavior: 'smooth',
          block: 'start'
        })
      }
    }
  }
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background-color: rgba(10, 10, 10, 0);
  /* backdrop-filter: blur(1px); */
  z-index: 1000;
  padding: 1.5rem 0;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--text);
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  color: var(--text);
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: var(--accent);
}
</style> 