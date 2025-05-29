<template>
  <div class="home">
    <h1>CI CD 가 잘 된다는 증거입니다. 당신을 축복합니다. 힘내세요.</h1>
    <div class="button-container">
      <button @click="$router.push('/test')" class="test-button">테스트 페이지로 이동</button>
      <button @click="$router.push('/portfolio')" class="portfolio-button">포트폴리오 보기</button>
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
  padding: 2rem;
}

.button-container {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 1rem;
}

.test-button, .portfolio-button {
  padding: 1rem 2rem;
  font-size: 1.2rem;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
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
</style> 