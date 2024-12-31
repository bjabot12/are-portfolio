<template>
  <footer class="footer">
    <div class="container footer-content">
      <div class="footer-logo">
        <img src="@/assets/images/ENK_LOGO_LITEN_BLÅ.png" alt="ENK Logo" class="logo-image">
      </div>
      <div class="footer-links">
        <router-link to="/">PROSJEKTER</router-link>
        <router-link to="/about">OM</router-link>
        <router-link to="/contact">KONTAKT</router-link>
      </div>
      <div class="social-links">
        <a href="https://www.linkedin.com" target="_blank" rel="noopener">
          <img src="@/assets/images/linkedin.webp" alt="LinkedIn" class="social-icon">
        </a>
        <a href="https://www.instagram.com" target="_blank" rel="noopener">
          <img src="@/assets/images/insta.png" alt="Instagram" class="social-icon">
        </a>
        <a href="https://www.imdb.com" target="_blank" rel="noopener">
          <img src="@/assets/images/hvit_imdb.png" alt="IMDB" class="social-icon">
        </a>
      </div>
      <div class="copyright">
        © {{ new Date().getFullYear() }} Are Botnevik. All rights reserved.
        <br>
        Made by Botnevik Koding ENK
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.footer {
  background-color: var(--dark-bg);
  padding: 4rem 0;
  margin-top: auto;
}

.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.logo-image {
  height: 40px;
  width: auto;
}

.social-icon {
  width: 24px;
  height: 24px;
}

.footer-links, .social-links {
  display: flex;
  gap: 2rem;
}

.footer-links a {
  color: var(--text);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--accent);
}

.copyright {
  color: var(--text-secondary);
  font-size: 0.9rem;
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .footer {
    padding: 2rem 0;
  }

  .footer-links {
    align-items: center;
    gap: 1rem;
  }

  .social-links {
    gap: 1.5rem;
  }
}

  .social-icon {
    width: 20px;
    height: 20px;
  }

</style> 