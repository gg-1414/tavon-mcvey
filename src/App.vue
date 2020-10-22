<template>
  <div id="app">
    <Nav/>
    <QuickMenu/>
    <Home/>
    <Bio/>
    <Work/>
    <Gallery/>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import QuickMenu from './components/QuickMenu.vue'
import Home from './components/Home.vue'
import Bio from './components/Bio.vue'
import Work from './components/Work.vue'
import Gallery from './components/Gallery.vue'
import './styles/global.scss';

export default {
  name: 'App',
  components: {
    Nav,
    QuickMenu,
    Home,
    Bio,
    Work,
    Gallery,
  }
}
</script>

<style lang="scss">
  html {
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    height: 100%;

    > section {
      height: 100vh;
      width: 100%;
      scroll-snap-align: start;
      padding: 48px 0 0;
    }
  }

  .btn {
    border: 1px solid white;
    padding: 0 1rem;
  }

@media screen and (min-width: 768px) {
  #app {

  }
}
</style>
