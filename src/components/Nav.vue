<template>
  <div class="nav">
    <a href="#home">Home</a>
    <a href="#bio">Bio</a>
    <a href="#work">Work</a>
    <a href="#gallery">Gallery</a>
    <a>Videos</a>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
  .nav {
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
    .nav {
      a {
        padding: 0 1rem;
      }
    }
  }
</style>