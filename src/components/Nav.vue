<template>
  <nav>
    <template v-if="route === 'Home'"> 
      <a href="#hero">Home</a>
      <a href="#bio">Bio</a>
      <a href="#work">Work</a>
      <router-link to="/gallery">Gallery</router-link>
      <router-link to="/videos">Videos</router-link>
    </template>

    <template v-else>
      <router-link to="/">Back</router-link>
    </template>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  props: {
    route: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
  nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: white;
    padding: 1rem;
    display: flex;
    justify-content: space-evenly;
    z-index: 10;
    // box-shadow: 0px 3px 3px 0px #00000030;
    // border-bottom: 3px solid #555555;

    a {
      color: #2c3e50;
    }
  }

  @media screen and (min-width: 768px) {
    nav {
      a {
        padding: 0 1rem;
      }
    }
  }
</style>