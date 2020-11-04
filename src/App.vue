<template>
  <div id="app">
    <Nav :route="currentRoute"/>
    <QuickMenu/>
    <router-view/>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'
import QuickMenu from '@/components/QuickMenu.vue'
import '@/styles/global.scss';
import '@/styles/type.scss';

export default {
  name: 'App',
  components: {
    Nav,
    QuickMenu,
  },
  computed: {
    currentRoute() {
      return this.$route.name
    }
  }
}
</script>

<style lang="scss">
  html {
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
  }

  #app {
    font-family: Avenir, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    height: 100%;
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
