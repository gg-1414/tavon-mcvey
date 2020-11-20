<template>
  <section id="bio">
    <h2>ABOUT ME</h2>

    <div class="images-block">
      <agile>
        <!-- <div v-for="(slide, i) in slides" :key="i" class="slide">
          <img :src="slide.image" />
        </div> -->
        <div class="slide">
          <img src="../assets/zen-shot-mobile.jpeg" />
        </div>
        <div class="slide">
          <img src="../assets/building-jump-shot-mobile.jpeg" />
        </div>
        <div class="slide">
          <img src="../assets/ult-tag-green-screen.jpg" />
        </div>
        <template slot="prevButton">
          <left-arrow-icon/>
        </template>
        <template slot="nextButton">
          <right-arrow-icon/>
        </template>
      </agile>
    </div>

    <div class="content-block">
      <div class="specs">
        <h3>Age: 30 y/o</h3>
        <h3>Build: Athletic</h3>
        <h3>Height: 6’2 1/2</h3>
        <h3>Weight: 187 lbs</h3>
        <h3>Hair: Short-Black</h3>
      </div>
      <p class="message">
        Hi I’m Tavon! I have been a practitioner of parkour for the last 15 years and 3x consecutive speed USA 🇺🇸 Parkour Champion 👑🤴🏽. I was the captain of The Boys 🏴‍☠️, the first invited USA team to play 🗺 World Chase Tag 🌐. I have had the fortunate opportunity of traveling the world doing what I love.
      </p>
    </div>
  </section>
</template>

<script>
import { VueAgile } from 'vue-agile'
import LeftArrowIcon from './icons/LeftArrow.vue'
import RightArrowIcon from './icons/RightArrow.vue'

export default {
  name: 'Bio',
  components: { 
    agile: VueAgile,
    LeftArrowIcon,
    RightArrowIcon
  }
}
</script>

<style lang="scss" scoped>
  #bio {
    background-color: #959595;
    color: white;
    position: relative;
    display: grid;
    grid-template-rows: auto 1.5fr 2fr;

    > * {
      margin-bottom: 1rem;
    }

    &:after {
      content: "TAVON MCVEY";
      color: #c0c0c0;
      font-size: 40vh;
      position: absolute;
      top: 3rem;
      left: 0;
      opacity: 0.2;
      overflow: hidden;
      width: 100%;
      z-index: 0;
    }

    h2 {
      margin-top: 16px;
    }

    .images-block {
      overflow: hidden;
      z-index: 2;

      .agile-slides {
        align-items: flex-start;
      }
    }

    .content-block {
      overflow: hidden; 
      padding: 0 1rem;
      text-align: left;

      .specs {
        h3 {
          border-left: 2px solid #afdf63;
          padding: 2px 8px;
        }
      }

      .message {
        margin-top: 14px;
        max-width: calc(100% - 64px);
      }
    }
  }

  @media screen and (min-width: 375px) and (min-height: 667px) {
    #bio {
      &:after {
        top: 50%;
        transform: translateY(-50%);
      }

      h2 {
        margin-top: 32px; 
      }

      .content-block {
        padding: 1rem;

        .specs {
            display: grid;
            grid-template-columns: 1fr 1fr;

          h3 {
            padding: 8px;
          }
        }

        .message {
          font-size: 16px;
        }
      }
    }
  }

  @media screen and (min-width: 768px) {
    #bio {
      grid-template-rows: auto 1.5fr 1fr;

      > * {
        margin-bottom: 24px;
      }

      h2 {
        margin-top: 64px;
      }

      .content-block {
        padding: 20px 48px;

        .specs h3 {
          font-size: 20px;
          padding: 8px 16px;
        }

        .message {
          font-size: 20px;
          margin-top: 32px;
        }
      }
    }
  }
</style>

<style lang="scss">
  @media screen and (min-width: 768px) {
    #bio {
      .agile .agile__slides {
        align-items: flex-start;
      }
    } 
  }
</style>