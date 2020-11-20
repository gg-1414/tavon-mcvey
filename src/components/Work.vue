<template>
  <section id="work">
    <agile :dots="false">
      <div class="slide">
        <div class="content-block">
          <div class="text-block">
            <h2>Ultimate Tag</h2>
            <h3>Stunt Actor, Television, Fox</h3>
            <small>Role: Flow <span>|</span> 2019-2020</small>
          </div>
          <div class="image-block">
            <img src="../assets/ult-tag-poster-1.jpg" />
          </div> 
          <div class="text-block"> 
            <p>Ultimate Tag is an American sports entertainment obstacle course competition television series that involves contestants running through various indoor obstacle courses while professional taggers (yours truly) attempt to catch them. Check it out!</p>
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="content-block">
          <div class="text-block">
            <h2>World Chase Tag</h2>
            <h3>Stunts/Parkour, Competition</h3>
            <small>Role: Captain of the Boys <span>|</span> 2018-2019</small>
          </div>
          <div class="image-block">
            <img src="../assets/WCT.jpg" />
            <!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/A3_Ieginod4?start=204" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
          </div> 
          <div class="text-block"> 
            <p>Captain of the Boys, World Chase Tag is an international championship for competitive parkour involving the game of tag.</p>
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="content-block">
          <div class="text-block">
            <h2>Porsche Launch Party</h2>
            <h3>Stunts/Parkour</h3>
            <small>Role: - <span>|</span> 2018-2019</small>
          </div>
          <div class="image-block">
            <img src="../assets/building-jump-shot-mobile.jpeg" />
          </div> 
          <div class="text-block"> 
            <p>Porsche Launch Party is this thing.</p>
          </div>
        </div>
      </div>
      <template slot="prevButton">
        <left-arrow-icon/>
      </template>
      <template slot="nextButton">
        <right-arrow-icon/>
      </template>
    </agile>
  </section>
</template>

<script>
import { VueAgile } from 'vue-agile'
import LeftArrowIcon from './icons/LeftArrow.vue'
import RightArrowIcon from './icons/RightArrow.vue'

export default {
  components: { 
    agile: VueAgile,
    LeftArrowIcon,
    RightArrowIcon
  },
}
</script>

<style lang="scss" scoped>
  #work {
    background-color: #1E1E1E;
    color: white;
    position: relative;

    &:after {
      content: "TAVON MCVEY";
      color: #646464;
      font-size: 40vh;
      position: absolute;
      top: 3rem;
      left: 0;
      opacity: 0.2;
      overflow: hidden;
      width: 100%;
      z-index: 0;
    }

    iframe {
      width: 100%;
    }

    h2 {
      margin-top: 16px;
    }

    h3 {
      padding: 2px 0;
    }

    .content-block {
      height: 90vh;
      padding: 0 1rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .text-block {
      p {
        max-width: calc(100% - 64px);
      }
    }

    .image-block {
      width: calc(100% - 64px);
      margin: auto;
      margin: 16px auto;
    }
  }

  @media screen and (min-width: 375px) and (min-height: 667px) {
    #work {
      &:after {
        top: 50%;
        transform: translateY(-50%);
      }

      h2 {
        margin-top: 32px; 
      }

      .text-block:last-child {
        padding: 1rem 2rem 1rem;

        p {
          max-width: calc(100% - 32px);
        }
      }
    }
  }

  @media screen and (min-width: 768px) {
    #work {
      h2 {
        margin-top: 64px;
      }
      
      .text-block {
        h3 {
          margin: 8px auto;
        }
        small {
          font-size: 16px;
        }
      }
      
      .image-block {
        width: calc(100% - 16rem);
        margin: 40px auto;
      }
    }
  }

  @media screen and (min-width: 768px) {
    #work {
      .image-block {
        width: calc(100% - 60rem);
      }
    }
  }
</style>
