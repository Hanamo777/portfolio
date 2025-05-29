<template>
  <div class="test">
    <h1>테스트 페이지</h1>
    <p>CI CD 가 잘 된다는 것을 보여주는 페이지입니다. 보이지 않는 손길이 당신을 인도하시기를</p>
    <button @click="$router.push('/')" class="home-button">홈으로 돌아가기</button>
  </div>
</template>

<script>
export default {
  name: 'TestView'
}
</script>

<style scoped>
.test {
  text-align: center;
  padding: 2rem;
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
}

.home-button:hover {
  background-color: #1976D2;
}
</style> 