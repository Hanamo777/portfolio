<template>
  <div class="home">
    <h1>포트폴리오를 보시려면 버튼을 누르세요.</h1>
    <div class="button-container">
      <button @click="$router.push('/test')" class="test-button">테스트 페이지로 이동</button>
      <button @click="$router.push('/portfolio')" class="portfolio-button">포트폴리오 보기</button>
      <a href="https://github.com/Hanamo777/Jenkins" target="_blank" class="github-button">GitHub 보기</a>
      <a href="https://blog.naver.com/hanamo7777777" target="_blank" class="blog-button">블로그 보기</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
.home {
  text-align: center;
  padding: 1rem;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.button-container {
  display: flex;
  gap: 2rem;
  justify-content: center;
  margin-top: 2rem;
  width: 100%;
  max-width: 1000px;
  flex-wrap: wrap;
}

.test-button, .portfolio-button, .github-button, .blog-button {
  padding: 1.2rem 3rem;
  font-size: 1.4rem;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s;
  flex: 1;
  max-width: 300px;
  text-decoration: none;
  display: inline-block;
}

.test-button {
  background-color: #4CAF50;
}

.test-button:hover {
  background-color: #45a049;
}

.portfolio-button {
  background-color: #2196F3;
}

.portfolio-button:hover {
  background-color: #1976D2;
}

.github-button {
  background-color: #333;
}

.github-button:hover {
  background-color: #555;
}

.blog-button {
  background-color: #03C75A;
}

.blog-button:hover {
  background-color: #02b351;
}
</style> 