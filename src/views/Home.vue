<template>
  <main id="home">
    <Hero/>
    <Bio/>
    <Work/>
    <Footer/>
    <div class="parallax">
      <img src="../assets/WCT.gif"/>
    </div>
  </main>
</template>

<script>
import Hero from '@/components/Hero.vue'
import Bio from '@/components/Bio.vue'
import Work from '@/components/Work.vue' 
import Footer from '@/components/Footer.vue'
import '@/styles/agile.scss';

export default {
  name: 'Home',
  components: {
    Hero,
    Bio,
    Work,
    Footer
  }
}
</script>

<style lang="scss" scoped>
  #home {
    > section {
      height: 100vh;
      width: 100%;
      scroll-snap-align: start;
      padding: 48px 0 0;
    }

    .parallax {
      position: fixed;
      bottom: 0;
      z-index: -1;
    }
  }
</style>