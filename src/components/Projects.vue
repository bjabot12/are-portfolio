<template>
  <section id="work" class="section projects">
    <div class="container">
      <div class="projects-list">
        <div v-for="project in projects" :key="project.id" class="project-item">
          <div class="project-header">
            <h3 class="project-title">{{ project.title }}</h3>
            <span class="project-description">{{ project.description }}</span>
          </div>
          <div class="project-images">
            <div v-for="(image, index) in project.images" 
                 :key="index" 
                 class="project-image-container"
                 >

              <img :src="require(`@/assets/images/${image}`)" :alt="`${project.title} image ${index + 1}`" class="project-image">
              <!-- <div class="image-overlay">
                <span v-if="index === 0" class="play-button">▶ Watch</span>
              </div> -->
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Video Modal -->
    <!-- <div class="video-modal" v-if="activeVideo" @click="closeVideo">
      <div class="modal-content" @click.stop>
        <button class="close-btn" @click="closeVideo">&times;</button>
        <div class="video-wrapper">
          <iframe
            :src="getVimeoEmbedUrl(activeVideo.vimeoId)"
            width="100%"
            height="100%"
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div> -->
  </section>
</template>

<script>
export default {
  name: 'ProjectsSection',
  data() {
    return {
      activeVideo: null,
      projects: [
        {
          id: 1,
          title: "PSYCHO KILLER ",
          description: "- KORTFILM",
          images: [
            "PK_1.png",
            "PK_2.png",
            "PK_3.png"
          ],
          vimeoId: "347119375"
        },
        {
          id: 2,
          title: "DET VAR EN GANG EN FJORD",
          description: "- KORTDOKUMENTAR",
          images: [
            "DVEGEF_5.png",
            "DVEGEF_1.png",
            "DVEGEF_7.png"
          ],
          vimeoId: "347119375"
        },        {
          id: 3,
          title: "AKTIV ALDRING",
          description: "- MILJØPORTRETT",
          images: [
            "AA_2.png",
            "AA_1.png",
            "AA_3.png"
          ],
          vimeoId: "347119375"
        },
      ]
    }
  },
  methods: {
    openVideo(project) {
      this.activeVideo = project;
      document.body.style.overflow = 'hidden';
    },
    closeVideo() {
      this.activeVideo = null;
      document.body.style.overflow = '';
    },
    getVimeoEmbedUrl(vimeoId) {
      return `https://player.vimeo.com/video/${vimeoId}?autoplay=1&title=0&byline=0&portrait=0`;
    }
  }
}
</script>

<style scoped>
.projects {
  background-color: var(--dark-bg);
  padding: 8rem 0;
}

.section-title {
  font-size: 3rem;
  margin-bottom: 4rem;
  text-align: center;
  background: linear-gradient(90deg, var(--accent), #00C6FF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.projects-list {
  display: flex;
  flex-direction: column;
  gap: 6rem;
}

.project-item {
  max-width: 1500px;
  margin: 0 auto;
}

.project-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 2rem;
}

.project-title {
  font-size: 1.5rem;
  color: var(--text);
  margin: 0;
}

.project-description {
  color: var(--text-secondary);
  font-size: 1.5rem;
}

.project-images {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  /* max-width: 2400px; */
  margin: 0 auto;
  /* padding: 0 2rem; */
}

.project-image-container {
  position: relative;
  aspect-ratio: 16/9;
  overflow: hidden;
  /* border-radius: 12px; */
  /* cursor: pointer; */
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-image-container:hover .project-image {
  transform: scale(1.05);
}

.play-button {
  color: white;
  font-size: 1.2rem;
  padding: 0.8rem 1.5rem;
  border: 2px solid white;
  border-radius: 30px;
  background: rgba(0, 0, 0, 0.5);
}

/* Video Modal Styles */
.video-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.9);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  width: 90%;
  max-width: 1200px;
  position: relative;
}

.video-wrapper {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  background: var(--dark-bg);
  border-radius: 12px;
  overflow: hidden;
}

.video-wrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.close-btn {
  position: absolute;
  top: -40px;
  right: -40px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: var(--accent);
  border: none;
  color: white;
  font-size: 24px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

@media (max-width: 768px) {
  .project-header {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .project-images {
    grid-template-columns: 1fr;
  }
}
</style> 