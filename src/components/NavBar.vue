<template>
    <nav class="navbar" :class="{ 'on-contact': isContactPage }">
      <div class="container nav-container">
        <router-link to="/" class="logo">
          <img :src="logoSource" alt="ENK Logo" class="logo-image">
        </router-link>
        <div class="nav-links">
          <router-link to="/" exact-active-class="active"><b>PROSJEKTER</b></router-link>
          <router-link to="/about" active-class="active"><b>OM</b></router-link>
          <router-link to="/contact" active-class="active"><b>KONTAKT</b></router-link>
        </div>
      </div>
    </nav>
  </template>

<script>
export default {
  name: 'NavBar',
  computed: {
    isContactPage() {
      return this.$route.path === '/contact'
    },
    logoSource() {
      return this.isContactPage 
        ? require('@/assets/images/ENK_LOGO_HVIT.png')
        : require('@/assets/images/ENK_LOGO_BLÅ.png')
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
  z-index: 1000;
  padding: 1.5rem 0;
  font-size: 1.5rem;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.logo {
  font-weight: 700;
  color: var(--text);
  text-decoration: none;
}

.logo-image {
  height: 40px;
  width: auto;
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

.nav-links .active {
  color: var(--accent);
}

.on-contact .nav-links a:hover {
  color: black;
}

.on-contact .nav-links .active {
  color: black;
}

@media (max-width: 768px) {
  .navbar {
    padding: 1rem 0;
    font-size: 1rem;
  }

  .nav-container {
    padding: 0 1rem;
  }

  .logo-image {
    height: 20px;
  }

  .nav-links {
    gap: 1rem;
  }
}
</style> 