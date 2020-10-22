<template>
  <section id="home">
    <div class="image-block">
      <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/hero.jpg" />
    </div>

    <div class="content-block">
      <h1>Tavon Mcvey</h1>
      <h2>"The Flow"</h2>
      <p>Tracuer / Actor / Stuntman</p>
      <p>Location: LA</p>

      <div class="ctas-block">
        <button>Call</button>
        <button>Email</button>
      </div>

      <div class="socials-block">
        <a href="facebook.com">
          <Facebook/>
        </a>
        <a href="twitter.com">
          <Twitter/>
        </a>
        <a href="instagram.com">
          <Instagram/>
        </a>
        <a href="youtube.com">
          <Youtube/> 
        </a>
      </div>
    </div>
  </section> 
</template>

<script>
import Facebook from './icons/Facebook.vue'
import Twitter from './icons/Twitter.vue'
import Instagram from './icons/Instagram.vue'
import Youtube from './icons/Youtube.vue'

export default {
  name: 'Home',
  components: {
    Facebook,
    Twitter,
    Instagram,
    Youtube
  }
}
</script>

<style lang="scss" scoped>
  #home {
    display: flex;
    flex-direction: column;

    .image-block {
      max-height: 500px;
      overflow: hidden;
      flex: 2;

      img {
        width: 100%;
      }
    }

    .content-block {
      flex: 1;
      display: grid;
      gap: .5rem;
      background: linear-gradient(45deg, black, #afdf63);
      background: linear-gradient(-45deg, #2F301E, #afdf63);
      background: linear-gradient(-45deg, #afdf63, #341b91);
      background-size: 400% 400%;
      background-size: 200% 100%;
      animation: gradient 10s ease infinite;
      padding: 1rem;
      color: white;
      text-align: left;

      .socials-block {
        display: flex; 
        justify-content: space-around;
        max-width: calc(100% - 88px);

        a {
          max-width: 32px;
          width: 32px;
        }
      }
    }
  }

  @media screen and (max-width: 767px) {
    #home {
      .ctas-block {
        display: none;
      }
    }
  }

  @media screen and (min-width: 768px) {
    #home {
      display: grid;
      grid-template-columns: auto 1fr;
      overflow: hidden;

      .image-block {
        img { 
          height: 100%; 
        }
      }

      .content-block {
        flex: 1;
        object-fit: fill;
      }
    }
  }

  @keyframes gradient {
    0%   { background-position:   0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position:   0% 50%; }
  }
</style>
