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
              <img src="@/assets/images/Are.jpg" alt="Are Botnevik" />
              <div class="image-overlay"></div>
            </div>
          </div>
        </div>
        <div class="projects-list">
          <h3 class="projects-title">Selected Projects</h3>
          <div class="project-entries">
            <div v-for="project in projects" :key="project.year" class="project-entry">
              <span class="project-year">{{ project.year }}</span>
              <h4 class="project-title">{{ project.title }}</h4>
              <span class="separator">-</span>
              <p class="project-description">{{ project.description }}</p>
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
        ],
        projects: [
          {
            year: '2023',
            title: 'The Silent Forest',
            description: 'A documentary exploring the hidden life of Norways ancient woodlands.'
          },
          {
            year: '2022',
            title: 'Urban Rhythms',
            description: 'A visual journey through Oslos evolving cityscape and culture.'
          },
          {
            year: '2021',
            title: 'Northern Lights',
            description: 'An intimate portrait of life above the Arctic Circle.'
          }
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
    /* border-radius: 24px; */
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
    /* border-radius: 12px; */
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
    /* border-radius: 24px; */
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
    /* background: linear-gradient(45deg, rgba(0, 122, 255, 0.2), transparent); */
  }
  
  .image-container:hover img {
    transform: scale(1.05);
  }
  
  .projects-list {
    margin-top: 4rem;
    /* max-width: 800px; */
  }
  
  .projects-title {
    font-size: 2rem;
    margin-bottom: 2rem;
    color: var(--text);
  }
  
  .project-entries {
    display: flex;
    flex-direction: column;
    /* gap: 1.5rem; */
  }
  
  .project-entry {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding-bottom: 1.5rem;
    /* border-bottom: 1px solid rgba(255, 255, 255, 0.2); */
  }
  
  .project-year {
    color: var(--accent);
    font-size: 1.3rem;
    /* white-space: nowrap; */
  }
  
  .separator {
    color: rgba(255, 255, 255, 0.6);
    font-size: 1.2rem;
  }
  
  .project-title {
    color: white;
    font-size: 1.3rem;
    /* font-family: 'Playfair Display', serif; */
    font-weight: 700;
    font-style: italic;
    margin: 0;
    white-space: nowrap;
  }
  
  .project-description {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1.3rem;
    margin: 0;
  }
  
  @media (max-width: 968px) {
    .project-entry {
      flex-wrap: wrap;
      gap: 0.75rem;
    }
    
    .project-year,
    .separator {
      font-size: 1rem;
    }
    
    .project-title {
      font-size: 1.4rem;
    }
    
    .project-description {
      font-size: 1rem;
      width: 100%;
      margin-top: 0.5rem;
    }
  }

  @media (max-width: 768px) {
    .project-header {
      gap: 0.75rem;
    }
    
    .project-year,
    .separator {
      font-size: 1rem;
    }
    
    .project-title {
      font-size: 1.4rem;
    }
    
    .project-description {
      font-size: 1rem;
    }
  }

  @media (max-width: 480px) {
    .stats {
      grid-template-columns: 1fr;
    }
  }
  </style> 