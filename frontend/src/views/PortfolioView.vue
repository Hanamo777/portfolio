<template>
  <div class="portfolio">
    <h1>포트폴리오</h1>
    <div class="image-container">
      <img :src="currentImage" :alt="'Slide ' + (currentIndex + 1)" class="slide-image">
    </div>
    <div class="controls">
      <button @click="prevSlide" class="nav-button" :disabled="currentIndex === 0">이전</button>
      <span class="slide-number">{{ currentIndex + 1 }} / {{ totalSlides }}</span>
      <button @click="nextSlide" class="nav-button" :disabled="currentIndex === totalSlides - 1">다음</button>
    </div>
    <button @click="$router.push('/')" class="home-button">홈으로 돌아가기</button>
  </div>
</template>

<script>
export default {
  name: 'PortfolioView',
  data() {
    return {
      currentIndex: 0,
      images: Array.from({ length: 22 }, (_, i) => 
        new URL(`../assets/slides/slide${i + 1}.JPG`, import.meta.url).href
      )
    }
  },
  computed: {
    currentImage() {
      return this.images[this.currentIndex]
    },
    totalSlides() {
      return this.images.length
    }
  },
  methods: {
    nextSlide() {
      if (this.currentIndex < this.totalSlides - 1) {
        this.currentIndex++
      }
    },
    prevSlide() {
      if (this.currentIndex > 0) {
        this.currentIndex--
      }
    }
  }
}
</script>

<style scoped>
.portfolio {
  text-align: center;
  padding: 2rem;
}

.image-container {
  margin: 2rem auto;
  max-width: 800px;
}

.slide-image {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.controls {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  margin: 1rem 0;
}

.nav-button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.nav-button:disabled {
  background-color: #cccccc;
  cursor: not-allowed;
}

.nav-button:not(:disabled):hover {
  background-color: #45a049;
}

.slide-number {
  font-size: 1.2rem;
  font-weight: bold;
}

.home-button {
  padding: 1rem 2rem;
  font-size: 1.2rem;
  background-color: #2196F3;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
  margin-top: 1rem;
}

.home-button:hover {
  background-color: #1976D2;
}
</style> 