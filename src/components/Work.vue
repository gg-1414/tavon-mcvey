<template>
  <section id="work">
    <VueAgile>
      <div class="slide">
        <div class="content-block">
          <div class="text-block">
            <h2>Ultimate Tag</h2>
            <h3>Stunt Actor, Television, Fox</h3>
            <small>Role: Flow <span>|</span> 2019-2020</small>
          </div>
          <div class="image-block">
            <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/ult-tag-poster-1.jpg" />
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
            <!-- <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/WCT.jpg" /> -->
            <iframe width="560" height="315" src="https://www.youtube.com/embed/A3_Ieginod4?start=204" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
            <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/building-jump-shot.jpg" />
          </div> 
          <div class="text-block"> 
            <p>Porsche Launch Party is this thing.</p>
          </div>
        </div>
      </div>
    </VueAgile>
  </section>
</template>

<script>
import { VueAgile } from 'vue-agile'

export default {
  components: { 
    VueAgile,
  },
  mounted() {
    const agile__actions = document.querySelector('.agile__actions') 
    agile__actions.style.position = "absolute"
    agile__actions.style.top = "50%"
    agile__actions.style.width = "100%"
    agile__actions.style.transform = "translateY(-75%)"

    const buttons = agile__actions.querySelectorAll('button')
    for (let i = 0; i < buttons.length; i++) {
      buttons[i].style.backgroundColor = "transparent"
      buttons[i].style.border = "none"
      buttons[i].style.color = "green"
      buttons[i].style.fontSize = "40px"
      buttons[i].style.padding = "12px"
    }
    buttons[0].innerText = "⇽"
    buttons[1].innerText = "⇾"

    agile__actions.querySelector('.agile__dots').style.display = "none"
  }
}
</script>

<style lang="scss" scoped>
  #work {
    background-color: #1E1E1E;
    color: white;
    position: relative;

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
      height: 100vh;
      padding: 0 1rem;
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
</style>
