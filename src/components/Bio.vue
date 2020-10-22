<template>
  <section id="bio">
    <h2>ABOUT ME</h2>

    <div class="images-block">
      <vueper-slides>
        <vueper-slide v-for="(slide, i) in slides" :key="i" :image="slide.image" />
      </vueper-slides>
    </div>

    <div class="content-block">
      <div class="specs">
        <h3>Age: </h3>
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
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  components: { 
    VueperSlides, 
    VueperSlide 
  },
  data: () => ({
    slides: [
      { image: 'https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/building-jump-shot.jpg' },
      { image: 'https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/ult-tag-green-screen.jpg' },
      { image: 'https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/zen-shot.jpg' }
    ]
  }),
  mounted() {
    document.querySelector('.vueperslides__inner').style.height = '100%';
    document.querySelector('.vueperslides__parallax-wrapper').style.paddingBottom = '58%';
  }
}
</script>

<style lang="scss" scoped>
  #bio {
    background-color: #959595;
    color: white;
    position: relative;
    display: grid;
    grid-template-rows: auto .5fr 2fr;
    gap: 1rem;

    &:after {
      content: "TAVON MCVEY";
      color: #c0c0c0;
      font-size: 40vh;
      position: absolute;
      top: 2rem;
      left: 0;
      opacity: 0.2;
      overflow: hidden;
      width: 100%;
    }

    h2 {
      margin-top: 1rem;
    }

    .images-block {
      .vueperslides,
      .vueperslides__inner {
        height: 100%;
      }

      .vueperslides__inner {
        height: 100%;
      }
    }

    .content-block {
      overflow: hidden; 
      padding: 0 1rem;
      text-align: left;

      .message {
        margin-top: 14px;
        max-width: calc(100% - 64px);
      }
    }
  }
</style>