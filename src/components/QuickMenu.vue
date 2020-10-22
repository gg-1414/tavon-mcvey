<template>
  <div class="quick-menu">
    <button class="menu-toggle">
      <div class="menu-dots">
        <div class="dot"></div>
      </div>
    </button>
    <div class="menu-items">
      <a href="tel:2156263411">
        <Phone/>
      </a>
      <a href="mailto:tavon.mcvey@gmail.com">
        <Email/>
      </a>
      <a href="https://www.facebook.com/TavonFlows/">
        <Facebook/>
      </a>
    </div>
  </div>
</template>

<script>
import Phone from './icons/Phone.vue'
import Email from './icons/Email.vue'
import Facebook from './icons/Facebook.vue'

export default {
  name: 'QuickMenu',
  components: {
    Phone,
    Email,
    Facebook
  }
}
</script>

<style lang="scss" scoped>
  .quick-menu {
    position: fixed;
    width: 3.5rem;
    height: 3.5rem;
    bottom: 1.5rem;
    right: 1.5rem;
    z-index: 98;

    button.menu-toggle {
      border-radius: 50%;
      background-color: #341b91;
      box-shadow: 0px 2px 8px 0px rgba(0,0,0,0.3);
      padding: 0;
      height: 100%;
      width: 100%;
      border: 0;
    }

    .menu-dots {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
    }

    .dot {
      position: relative;

      &,
      &:before,
      &:after {
        position: absolute;
        width: 6px;
        height: 6px;
        border-radius: 1.25rem;
        background-color: white;
      }

      &:before,
      &:after {
        content: "";
        transition: left .3s ease-out, width .3s ease-out;
      }

      & {
        left: 50%;
        transform: translateX(-50%);
      }

      &:before {
        left: 10px;
      }

      &:after {
        left: -10px;
      }
    }

    .menu-items {
      display: none;
    }
  }

  @media screen and (min-width: 768px) {
    .quick-menu {
      display: none;
    }
  }
</style>
