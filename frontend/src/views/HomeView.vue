<template>
  <div class="home">
    <h1>CI CD 가 잘 된다는 증거입니다. 당신을 축복합니다. 힘내세요.</h1>
    <button @click="$router.push('/test')" class="test-button">테스트 페이지로 이동</button>
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

.test-button {
  padding: 1rem 2rem;
  font-size: 1.2rem;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.test-button:hover {
  background-color: #45a049;
}
</style> 