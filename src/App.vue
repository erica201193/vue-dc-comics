<template>
  <div id="app">

    <div class="bg-white">
      <div class="container">
        <TheHeader/>
      </div>
    </div>
    
    <div class="jumbo-bg-image">
      <img src="/img/jumbotron.jpg" alt="">
    </div>

    <div class="bg-main">
      <div class="container">
        <TheMain></TheMain>
      </div>
    </div>


    <TheFooter/>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';



export default {
  name: 'App',
  components: { TheHeader, TheMain, TheFooter}
}
</script>

<style lang="scss">
@import "assets/scss/main.scss";
#app {
  font-family: 'Asap Condensed', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  .bg-main {
    background-color: #1C1C1C;
  }

  .jumbo-bg-image {
    & img {
      width: 100%;
      height: 400px;
      object-fit: none;
      object-position: top;
    }
  }
}
</style>
