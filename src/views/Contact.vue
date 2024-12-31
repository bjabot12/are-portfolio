<template>
  <section id="contact" class="section contact">
    <div class="container">
      <h1 class="section-title">Hei! Kult at du er innom nettsiden min. Ikke nøl med å ta kontakt :) </h1>
      <div class="contact-info">
        <div class="contact-methods">
          <div class="method-details">
            <h4>Mail</h4>
            <p><a href="mailto:are@enkproduksjon.no">are@enkproduksjon.no</a></p>
          </div>
          <div class="method-details">
            <h4>Mobil</h4>
            <p><a href="tel:+4792223344">+47 922 23 344</a></p>
          </div>
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
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style>
.contact {
  background-color: #004FFF;
  /* padding: 8rem 0; */
  min-height: 100vh;
  display: flex;
  align-items: center;
  color: white;
}

.container {
  max-width: 1800px;
  margin: 0 auto;
  padding: 0 4rem;
  text-align: center;
}

.section-title {
  font-size: 2rem;
  /* margin-bottom: 5rem; */
  color: white;
  font-weight: 600;
}

.contact-info {
  max-width: 1200px;
  margin: 0 auto;
}

.contact-methods {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 4rem;
}

.method-details {
  text-align: center;
}

.method-details h4 {
  color: rgba(255, 255, 255, 0.6);
  font-size: 1.4rem;
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.method-details a,
.method-details p {
  color: white;
  text-decoration: none;
  font-size: 1.8rem;
  transition: color 0.3s ease;
  font-weight: 500;
}

.method-details a:hover {
  color: rgba(255, 255, 255, 0.8);
}

@media (max-width: 1200px) {
  .contact-methods {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .container {
    padding: 0 2rem;
  }
  
  .section-title {
    font-size: 3rem;
    margin-bottom: 3rem;
  }
  
  .contact-methods {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .method-details a,
  .method-details p {
    font-size: 1.4rem;
  }
  
  .method-details h4 {
    font-size: 1.2rem;
  }
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 3rem;
  margin-top: 5rem;
}

.social-icon {
  width: 60px;
  height: 60px;
  transition: opacity 0.3s ease;
}

.social-icon:hover {
  opacity: 0.8;
}

@media (max-width: 768px) {
  .social-links {
    margin-top: 3rem;
    gap: 2rem;
  }
  
  .social-icon {
    width: 28px;
    height: 28px;
  }
}
</style> 