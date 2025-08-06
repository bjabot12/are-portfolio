<template>
    <section id="about" class="section about">
      <div class="container">
        <div class="about-content">
          <div class="left-column">
            <div class="glass-card">
              <p class="bio">Jeg er en frilans filmfotograf med bachelorgrad i TV- og dokumentarproduksjon fra TV-skolen i Lillehammer. Som fotograf er jeg opptatt av å skape den rette visuelle stemningen for å løfte prosjektet og gi det mer dybde. Jeg ønsker å skape et univers hvor publikum kan glemme tid og sted og kjenne på nærhet og tilstedeværelse.
I tillegg har jeg mye erfaring med klipp og grade, noe som gir meg en større forståelse for alle ledd i produksjonen. </p>
 </div>
            
            <!-- <div class="education-section">
              <h3 class="section-subtitle">UTDANNING</h3>
              <div class="education-entries">
                <div v-for="edu in education" :key="edu.year" class="education-entry">
                  <span class="entry-year">{{ edu.year }}</span>
                  <h4 class="entry-title">{{ edu.degree }}</h4>
                  <p class="entry-description">{{ edu.school }}</p>
                </div>
              </div>
            </div> -->

            <div class="expertise-section">
              <h3 class="section-subtitle">FERDIGHETER</h3>
              <div class="expertise-entries">
                <div v-for="skill in skills" :key="skill.name" class="expertise-entry">
                  <span class="expertise-icon">{{ skill.icon }}</span>
                  <!-- <span class="separator">-</span> -->
                  <h4 class="expertise-title">{{ skill.name }}</h4>
                  <!-- <span class="separator">-</span>
                  <p class="expertise-description">{{ skill.description }}</p> -->
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
          <h3 class="section-subtitle">REFERANSEPROSJEKTER</h3>
          <div class="project-entries">
            <div v-for="project in projects" :key="project.year" class="project-entry">
              <span class="project-year">{{ project.year }}</span>
              <h4 class="project-title">{{ project.title }}</h4>
              <!-- <span class="separator">-</span> -->
              <p class="project-description">{{ project.description }}</p>
            </div>
          </div>

          <h3 class="section-subtitle">HØYDEPUNKT</h3>
          <div class="highlights-entries">
            <div v-for="highlight in highlights" :key="highlight.project" class="highlight-entry">
              <h4 class="highlight-title">{{ highlight.project }}</h4>
              <div class="nominations-list">
                <div v-for="(nomination, index) in highlight.nominations" :key="index" 
                     class="nomination-item">
                  <span class="nomination-text">{{ nomination }}</span>
                </div>
              </div>
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
        education: [
          {
 
          },
          {
            year: '2022-2025',
            title: 'KUNSTIG UINTELLIGENS',
            description: '  |  HUMORSERIE  |  A-FOTO'
          },
          {
            year: '🎓',
            degree: 'BACHELORGRAD I TV- OG DOKUMENTARPRODUKSJON',
            school: 'FOTO'
          },
          {
            year: '📍',
            degree: 'FAKULTET FOR FILM, TV OG SPILL',
            school: 'UNIVERSITETET I INNLANDET'
          },
          {

          }
        ],
        skills: [
          { 
            name: 'FOTO', 
            icon: '🎥',
          },
          { 
            name: 'GRADE', 
            icon: '🎨',
          },
          { 
            name: 'KLIPP', 
            icon: '✂️',
          },
          { 
            name: 'STILLSFOTO', 
            icon: '📷',
            description: 'Crafting immersive audio environments'
          },
          { 
            name: 'ADOBE SUITE OG DAVINCI RESOLVE STUDIO', 
            icon: '🖥️',
          },
          { 
            name: 'DRONE A1/A3', 
            icon: '👨‍✈️',
            
          }
        ],
        projects: [
          {
            year: '2025',
            title: 'RUNA',
            description: '  |  SPILLEFILM  |  KAM.ASS'
          },
          {
            year: '2025',
            title: 'MIDNATTSMØTET',
            description: '  |  KORTFILM  |  B-FOTO'
          },
          {
            year: '2025',
            title: 'ETT SISTE KAPITTEL',
            description: '  |  KORTDOKUMENTAR  |  FOTO / KLIPP / GRADE'
          },
          {
            year: '2024',
            title: 'KUNSTIG UINTELLIGENS',
            description: '  |  HUMORSERIE  |  DOP'
          },
          {
            year: '2024',
            title: 'PSYCHO KILLER',
            description: '  |  KORTFILM  |  FILMFOTOGRAF'
          },
          {
            year: '2024',
            title: 'KATASTROFE',
            description: '  |  DOKUMENTARSERIE  |  TEDDY TV  |  B.KAM / TEK.ASS'
          },
          {
            year: '2024',
            title: 'DET VAR EN GANG EN FJORD',
            description: '|  KORTDOKUMENTAR  | FOTO / KLIPP / GRADE'
          },
          {
            year: '2024',
            title: 'APPLAUS',
            description: '| KORTFILM | DEN NORSKE FILMSKOLEN  |  GRIP'
          },
          {
            year: '2023',
            title: 'AKTIV ALDRING',
            description: '|  KORTDOKUMENTAR  |  FOTO'
          },
          {
            year: '2023',
            title: 'BAK KASSA',
            description: '|  KORTDOKUMENTAR  |  KLIPP'
          },
          {
            year: '2023',
            title: 'ADHD-MIN SUPERKRAFT',
            description: '|  KORTDOKUMENTAR  |  FOTO / KLIPP'
          },
          {
            year: '2023',
            title: 'VINTERSPILL',
            description: '|  MUSIKKFESTIVAL  |  STILLSFOTO'
          },
        ],
        highlights: [
          {
            project: 'DET VAR EN GANG EN FJORD',
            nominations: [
              'AMANDUS BLIKKFANG | PUBLIKUMSPRISEN 2024',
              'BIFF | NOMINERT: BESTE NORSKE KORTDOKUMENTAR 2024',
              'NORDIC DOCS | NOMINERT: BESTE KORTDOKUMENTAR 2024',
              'DEN KULTURELLE SKOLESEKKEN | TURNÈ PÅ VESTLANDET 2024'
            ]
          },
          
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
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    width: 100%;
    box-sizing: border-box;
  }
  
  .about-content {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 4rem;
    align-items: start;
  }
  
  .left-column {
    display: flex;
    flex-direction: column;
    gap: 3rem;
  }
  
  .glass-card {
    background: rgba(255, 255, 255, 0.03);
    border-radius: 24px;
    padding: 2.5rem;
    width: 100%;
    box-sizing: border-box;
    overflow: hidden;
  }
  
  .bio {
    font-size: 1.2rem;
    line-height: 1.8;
    color: var(--text-secondary);
    word-break: break-word;
    overflow-wrap: break-word;
    hyphens: auto;
    max-width: 100%;
    white-space: normal;
    display: block;
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
  }
  
  .image-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* background: linear-gradient(45deg, rgba(0, 122, 255, 0.2), transparent); */
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
      /* flex-wrap: wrap; */
      gap: 0.4rem;
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
      max-width: 100%;
      /* margin-top: 0.5rem; */
    }
     .image-container img {
        width: 100%;
        height: 100%;
        /* object-fit: cover; */
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
    
    .project-description {
      font-size: 1rem;
    }
  }

  @media (max-width: 480px) {

    .project-description {
      font-size: .3rem;
    }
    .stats {
      grid-template-columns: 1fr;
    }
  }

  .expertise-entries {
    display: flex;
    flex-direction: column;
    /* gap: 1.5rem; */
  }

  .expertise-entry {
    display: flex;
    align-items: center;
    /* width: 100%; */
    /* gap: 1rem; */
    /* padding-bottom: 1.5rem; */
    /* border-bottom: 1px solid rgba(255, 255, 255, 0.2); */
  }

  .expertise-section {
    width: 170%;
  }

  .expertise-icon {
    font-size: 1rem;
    white-space: nowrap;
  }

  .separator {
    color: rgba(255, 255, 255, 0.6);
    font-size: 1.2rem;
  }

  .expertise-title {
    color: white;
    font-size: 1rem;
    /* font-family: 'Playfair Display', serif; */
    font-weight: 700;
    /* font-style: italic; */
    margin: 0;
  }

  .expertise-description {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1rem;
    margin: 0;
    flex: 1;
  }

  h3.expertise-title {
    font-size: 2rem;
    color: white;
    margin-bottom: 2rem;
  }

  @media (max-width: 968px) {
    .about {
      padding: 2rem 0;
    }

    .container {
      padding: 0 1rem;
      /* max-width: 100vw; */
      overflow-x: hidden;
    }

    .about-content {
      /* grid-template-columns: 1fr; */
      margin-top: 2rem;
      gap: .5rem;
    }

    .left-column {
      gap: 2rem;
    }

    .glass-card {
      margin-top: 1rem;
      padding: 1rem;
      margin: 0;
      border-radius: 12px;
      width: 93%;
    }

    .bio {
      font-size: 0.9rem;
      line-height: 1.6;
      padding-right: 0;
      width: 100%;
    }

    .section-subtitle {
      font-size: 1.2rem;
      margin-bottom: 1rem;
    }

    .entry-year,
    .entry-title,
    .entry-description,
    .expertise-title,
    .expertise-icon {
      font-size: 0.9rem;
    }

    .project-year,
    .project-title,
    .project-description {
      font-size: 0.9rem;
    }

    .highlight-title {
      font-size: 1rem;
    }

    .nomination-item {
      font-size: 0.9rem;
    }

    .nominations-list {
      margin-left: 0.5rem;
    }
  }

  @media (max-width: 480px) {
    .about {
      padding: 1.5rem 0;
      padding-top: 4rem;
    }

    .section-subtitle {
      font-size: 1.1rem;
    }

    .glass-card {
        width: 93%;
    }

    .project-description {
      font-size: .8rem;
    }

    .project-title {
      font-size: .8rem;
    }
  }

  .section-subtitle {
    font-size: 2rem;
    color: white;
    margin-bottom: 2rem;
    text-align: left;
  }

  .education-entries,
  .expertise-entries {
    display: flex;
  }

  .entry-year {
    color: var(--accent);
    font-size: 1rem;
    white-space: nowrap;
  }

  .entry-title {
    color: white;
    font-size: 1rem;
    /* font-family: 'Playfair Display', serif; */
    font-weight: 700;
    /* font-style: italic; */
    margin: 0;
    white-space: nowrap;
  }

  .entry-description {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1rem;
    margin: 0;
  }

  @media (max-width: 968px) {
    
    .entry-title {
      font-size: 1rem;
    }

    .entry-description {
      font-size: 1rem;
    }

    .section-subtitle {
      font-size: 1.8rem;
      /* margin-bottom: 1.5rem; */
    }

    .separator {
      display: none;
    }
  }

  .nominations-list {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    margin-left: 1rem;
  }

  .nomination-item {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1.1rem;
  }

  .highlight-entry {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding-bottom: 1.5rem;
    /* border-bottom: 1px solid rgba(255, 255, 255, 0.2); */
  }

  .highlight-title {
    color: white;
    font-size: 1.3rem;
    /* font-family: 'Playfair Display', serif; */
    font-weight: 700;
    font-style: italic;
    margin: 0;
    text-align: left;
  }

  .nominations-list {
    display: flex;
    flex-direction: column;
    text-align: left;
    gap: 0.5rem;
    margin-left: 1rem;
  }

  .nomination-item {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1.1rem;
  }

  @media (max-width: 968px) {
    .highlight-title {
      font-size: 1.4rem;
    }

    .nominations-list {
      margin-left: 0;
    }

    .nomination-item {
      font-size: 1rem;
    }
  }
  </style> 