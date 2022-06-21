<template>
  <div id="app">
    <div class="bg-white">
      <div class="container">
        <TheHeader/>
      </div>
    </div>

    <div class="bg-content">
      <div class="container">
        <main>
            --> Content goes here
        </main>
      </div>
    </div>
    
    <TheFooter/>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: { TheHeader, TheFooter }
}
</script>

<style lang="scss">
@import "assets/scss/main.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  .bg-content {
    background-color: #1C1C1C;
  }

  main {
    padding: 2rem;
    color: white;
    font-weight: bold;
    font-size: 1.2rem;
  }
}
</style>
