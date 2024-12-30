<template>
    <section id="about" class="section about">
      <div class="container">
        <div class="about-content">
          <div class="about-text">
            <h2 class="section-title">About Me</h2>
            <div class="glass-card">
              <p class="bio">I'm Are Botnevik, a passionate filmmaker and visual storyteller. My work focuses on capturing authentic human stories through innovative cinematography and compelling narratives that resonate with audiences worldwide.</p>
              <div class="stats">
                <div class="stat-item">
                  <span class="stat-number">5+</span>
                  <span class="stat-label">Years Experience</span>
                </div>
                <div class="stat-item">
                  <span class="stat-number">50+</span>
                  <span class="stat-label">Projects</span>
                </div>
                <div class="stat-item">
                  <span class="stat-number">12</span>
                  <span class="stat-label">Awards</span>
                </div>
              </div>
              <div class="skills">
                <h3>Expertise</h3>
                <div class="skills-grid">
                  <div class="skill-item" v-for="(skill, index) in skills" :key="index">
                    <span class="skill-icon">{{ skill.icon }}</span>
                    <span class="skill-name">{{ skill.name }}</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="about-image">
            <div class="image-container">
              <img src="data:image/jpeg;base64,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" alt="Are Botnevik" />
              <div class="image-overlay"></div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'AboutSection',
    data() {
      return {
        skills: [
          { name: 'Documentary', icon: '🎥' },
          { name: 'Cinematography', icon: '📷' },
          { name: 'Video Editing', icon: '✂️' },
          { name: 'Storytelling', icon: '📖' },
          { name: 'Sound Design', icon: '🎧' },
          { name: 'Color Grading', icon: '🎨' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .about {
    background-color: var(--dark-bg);
    padding: 8rem 0;
    position: relative;
    overflow: hidden;
  }
  
  .about::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -20%;
    width: 80%;
    height: 200%;
    background: radial-gradient(circle, rgba(0, 122, 255, 0.05) 0%, transparent 70%);
    transform: rotate(-45deg);
  }
  
  .about-content {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 4rem;
    align-items: center;
  }
  
  .section-title {
    font-size: 3rem;
    margin-bottom: 2rem;
    background: linear-gradient(90deg, var(--accent), #00C6FF);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  
  .glass-card {
    background: rgba(255, 255, 255, 0.03);
    backdrop-filter: blur(10px);
    border-radius: 24px;
    padding: 2.5rem;
    border: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .bio {
    font-size: 1.2rem;
    line-height: 1.8;
    color: var(--text-secondary);
    margin-bottom: 2.5rem;
  }
  
  .stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin-bottom: 3rem;
    padding: 2rem 0;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .stat-item {
    text-align: center;
  }
  
  .stat-number {
    display: block;
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--accent);
    margin-bottom: 0.5rem;
  }
  
  .stat-label {
    color: var(--text-secondary);
    font-size: 0.9rem;
  }
  
  .skills h3 {
    margin-bottom: 1.5rem;
    font-size: 1.5rem;
    color: var(--text);
  }
  
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }
  
  .skill-item {
    background: rgba(255, 255, 255, 0.05);
    padding: 1rem;
    border-radius: 12px;
    text-align: center;
    transition: transform 0.3s ease;
  }
  
  .skill-item:hover {
    transform: translateY(-5px);
  }
  
  .skill-icon {
    font-size: 1.5rem;
    display: block;
    margin-bottom: 0.5rem;
  }
  
  .skill-name {
    color: var(--text-secondary);
    font-size: 0.9rem;
  }
  
  .image-container {
    position: relative;
    border-radius: 24px;
    overflow: hidden;
    aspect-ratio: 3/4;
  }
  
  .image-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }
  
  .image-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, rgba(0, 122, 255, 0.2), transparent);
  }
  
  .image-container:hover img {
    transform: scale(1.05);
  }
  
  @media (max-width: 968px) {
    .about-content {
      grid-template-columns: 1fr;
    }
    
    .stats {
      grid-template-columns: repeat(2, 1fr);
    }
    
    .skills-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  
  @media (max-width: 480px) {
    .stats {
      grid-template-columns: 1fr;
    }
  }
  </style> 