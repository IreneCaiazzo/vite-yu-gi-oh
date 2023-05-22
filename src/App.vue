<script>
import ResultsMessage from './components/ResultsMessage.vue';

export default {
  components: {
    ResultsMessage,
  },
}
</script>

<template>
  <header>
    <nav>
      <img src="https://3.bp.blogspot.com/-wLH_qbmRoJU/TZdYCkrQuZI/AAAAAAAAAw0/G1_uzsANMI8/s1600/yugioh+logo.png" alt="">
      <h1>Yu Gi Oh!</h1>
    </nav>
  </header>

  <main>
    <select name="alien" id=""></select>

    <div class="container">
      <ResultsMessage />
    </div>
  </main>
</template>

<style scoped>
header {
  height: 5rem;
}

nav {
  display: flex;
}

img {
  width: 150px;
}

main {
  background-color: orange;
  display: flex;
  flex-direction: column;
}

main select {
  width: 100px;
  margin-left: 3rem;
}

.container {

  width: 100px;
  height: 100px;
  justify-self: center;
  align-self: center;
  background-color: white;
}
</style>
