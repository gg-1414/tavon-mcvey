<template>
  <section id="hero">
    <div class="image-block">
      <img src="../assets/hero.jpg" />
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
  #hero {
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
      background: linear-gradient(-45deg, #afdf63, #341b91);
      background-size: 200% 100%;
      animation: gradient 10s ease infinite;
      padding: 1rem;
      color: white;

      > * {
        text-align: center;
      }

      h1, p {
        padding-bottom: .25rem;
      }

      h2 {
        padding-bottom: .75rem;
      }

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
    #hero {
      .ctas-block {
        display: none;
      }
    }
  }

  @media screen and (min-width: 375px) and (min-height: 667px) {
    #hero {
      .content-block, 
      p {
        text-align: center;
      }

      .content-block {
        padding: 1.5rem 1rem;
      }

      .socials-block {
        margin-top: 1rem;
      }
    }
  }

  @media screen and (min-width: 768px) {
    #hero {
      overflow: hidden;

      .image-block {
        max-height: initial;
        grid-area: image;
        flex: 3;
        position: relative;

        img {
          position: absolute;
          top: -50px;
          left: 0;
        }
      }

      .content-block {
        grid-area: content;
        object-fit: fill;

        h1, h2 {
          padding-bottom: 16px;
        } 
        
        p {
          padding-bottom: 8px;
        }

        .ctas-block {
          margin-top: 16px;

          button {
            margin: 0 6px;
          }
        }

        .socials-block {
          width: 100%;
          max-width: initial;
          justify-content: space-evenly;
          margin-top: 20px;
          max-width: 400px;
          margin: 20px auto 0;

          a {
            max-width: 40px;
            width: 40px;
          }
        }
      }
    }
  }

  @media screen and (min-width: 1280px) {
    #hero {
      flex-direction: row;

      .image-block {
        flex: 2;
      }

      .content-block {
        display: flex;
        flex-direction: column;

        h1 {
          flex: 1;
          display: flex;
          align-items: flex-end;
          justify-content: center;
        }

        .socials-block {
          flex: 1;
        }
      }
    }
  }

  @keyframes gradient {
    0%   { background-position:   0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position:   0% 50%; }
  }
</style>
