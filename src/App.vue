<script>
import ResultsMessage from './components/ResultsMessage.vue';
import CardsContainer from './components/CardsContainer.vue';
import axios from 'axios';
import { store } from './store';

export default {
  data() {
    return {
      store,
    };
  },

  components: {
    ResultsMessage,
    CardsContainer,
  },

  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(response => (this.store.arrCards = response.data.data));
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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  height: 5rem;
}

nav {
  display: flex;
  align-items: center;
  margin-inline: 1rem;
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
  margin: 2rem 3rem;
}

.container {
  width: 1000px;
  height: 100%;
  justify-self: center;
  align-self: center;
  background-color: white;
  margin-bottom: 2rem;
}
</style>
