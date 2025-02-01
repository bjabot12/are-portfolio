<template>
  <section id="contact" class="section contact">
    <div class="container">
      <h1 class="section-title">Hei! Kult at du er innom nettsiden min. Ikkje nøl med å ta kontakt :) </h1>
      <div class="contact-info">
        <div class="contact-methods">
          <div class="method-details">
            <h4>E-post</h4>
            <p><a href="mailto:arebotnevik@gmail.com">arebotnevik@gmail.com</a></p>
          </div>
          <div class="method-details">
            <h4>Mobil</h4>
            <p><a href="tel:+4748359533">+47 97747012</a></p>
          </div>
          <div class="method-details">
            <h4>Sted</h4>
            <div class="location-items">
              <p><span class="location-icon">📍</span>Oslo / Bergen</p>
            </div>
          </div>
        </div>
        <div class="social-links">
          <a href="https://no.linkedin.com/in/are-botnevik-1100312b9?trk=public_post_feed-actor-name" target="_blank" rel="noopener">
            <img src="@/assets/images/linkedin.webp" alt="LinkedIn" class="social-icon">
          </a>
          <a href="https://www.instagram.com/arebotnevik/" target="_blank" rel="noopener">
            <img src="@/assets/images/insta.png" alt="Instagram" class="social-icon">
          </a>
          <a href="https://www.imdb.com/name/nm16185899/?ref_=nv_sr_srsg_0_tt_0_nm_3_in_0_q_arebotnev" target="_blank" rel="noopener">
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
  grid-template-columns: repeat(3, 1fr);
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
    font-size: 1.8rem;
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

.locations {
  /* margin-top: 2rem; */
}

.location-items {
  display: flex;
  justify-content: center;
  align-items: center;
}

.location-items p {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--text);
  font-size: 1.6rem;
  margin: 0;
  padding-top: 0.6rem;
}

.location-icon {
  font-size: 1.2rem;
}

.location-text {
  display: inline-block;
}

@media (max-width: 768px) {
  .location-items {
    gap: 1rem;
  }
  
  .location-items p {
    font-size: 1rem;
  }
}
</style> 