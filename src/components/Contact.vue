<template>
  <section id="contact" class="section contact">
    <div class="container">
      <h2 class="section-title">Let's Create Together</h2>
      <div class="contact-content">
        <div class="contact-info">
          <div class="glass-card">
            <h3>Get in Touch</h3>
            <p>Ready to bring your vision to life? I'm always excited to discuss new projects and creative collaborations.</p>
            <div class="contact-methods">
              <div class="contact-method">
                <div class="method-icon">📧</div>
                <div class="method-details">
                  <h4>Email</h4>
                  <a href="mailto:are@botnevik.com">are@botnevik.com</a>
                </div>
              </div>
              <div class="contact-method">
                <div class="method-icon">📍</div>
                <div class="method-details">
                  <h4>Location</h4>
                  <p>Oslo, Norway</p>
                </div>
              </div>
            </div>
            <div class="social-links">
              <a href="#" class="social-link" target="_blank">
                <i class="fab fa-vimeo-v"></i>
              </a>
              <a href="#" class="social-link" target="_blank">
                <i class="fab fa-instagram"></i>
              </a>
              <a href="#" class="social-link" target="_blank">
                <i class="fab fa-linkedin-in"></i>
              </a>
            </div>
          </div>
        </div>
        <div class="contact-form-container">
          <form class="contact-form glass-card" @submit.prevent="handleSubmit">
            <div class="form-group">
              <label for="name">Name</label>
              <input 
                type="text" 
                id="name"
                v-model="form.name" 
                placeholder="Your name"
                required
              >
            </div>
            <div class="form-group">
              <label for="email">Email</label>
              <input 
                type="email" 
                id="email"
                v-model="form.email" 
                placeholder="Your email"
                required
              >
            </div>
            <div class="form-group">
              <label for="message">Message</label>
              <textarea 
                id="message"
                v-model="form.message" 
                placeholder="Tell me about your project"
                required
              ></textarea>
            </div>
            <button type="submit" class="submit-btn">
              Send Message
              <span class="btn-icon">→</span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    handleSubmit() {
      console.log('Form submitted:', this.form)
    }
  }
}
</script>

<style scoped>
.contact {
  background-color: var(--dark-bg);
  padding: 8rem 0;
  position: relative;
  overflow: hidden;
}

.contact::before {
  content: '';
  position: absolute;
  bottom: -50%;
  left: -20%;
  width: 80%;
  height: 200%;
  background: radial-gradient(circle, rgba(0, 122, 255, 0.05) 0%, transparent 70%);
  transform: rotate(45deg);
}

.section-title {
  font-size: 3rem;
  text-align: center;
  margin-bottom: 4rem;
  background: linear-gradient(90deg, var(--accent), #00C6FF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}

.glass-card {
  background: rgba(255, 255, 255, 0.03);
  backdrop-filter: blur(10px);
  border-radius: 24px;
  padding: 2.5rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.contact-info h3 {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: var(--text);
}

.contact-info p {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 2.5rem;
}

.contact-methods {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  margin-bottom: 2.5rem;
}

.contact-method {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.method-icon {
  font-size: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  padding: 1rem;
  border-radius: 12px;
}

.method-details h4 {
  color: var(--text);
  margin-bottom: 0.25rem;
}

.method-details a,
.method-details p {
  color: var(--text-secondary);
  margin: 0;
  text-decoration: none;
  transition: color 0.3s ease;
}

.method-details a:hover {
  color: var(--accent);
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 12px;
  color: var(--text);
  text-decoration: none;
  transition: all 0.3s ease;
}

.social-link:hover {
  background: var(--accent);
  transform: translateY(-3px);
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-group label {
  color: var(--text);
  font-size: 0.9rem;
}

.form-group input,
.form-group textarea {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  padding: 1rem;
  color: var(--text);
  font-size: 1rem;
  transition: all 0.3s ease;
}

.form-group textarea {
  min-height: 150px;
  resize: vertical;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--accent);
  background: rgba(255, 255, 255, 0.08);
}

.submit-btn {
  background: var(--accent);
  color: var(--text);
  border: none;
  padding: 1rem 2rem;
  border-radius: 12px;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}

.btn-icon {
  transition: transform 0.3s ease;
}

.submit-btn:hover {
  transform: translateY(-2px);
}

.submit-btn:hover .btn-icon {
  transform: translateX(5px);
}

@media (max-width: 968px) {
  .contact-content {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2.5rem;
  }
}

@media (max-width: 480px) {
  .glass-card {
    padding: 1.5rem;
  }
  
  .contact-methods {
    gap: 1rem;
  }
}
</style> 