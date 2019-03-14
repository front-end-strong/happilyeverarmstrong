<template>
  <nav>
    <a class="navigation__link navigation__toggle" v-bind:class="{'navigation__toggle--is-open':this.menuOpen}" v-on:click="toggleMenu">
      <span class="navigation__toggle--closed">menu</span>
      <span class="navigation__toggle--opened">X Close</span>
    </a>
    <ul class="navigation" v-bind:class="{'navigation--is-open':this.menuOpen}">
      <li class="navigation__link" v-on:click="toggleMenu"><a>The Journey so far</a></li>
      <li class="navigation__link" v-on:click="toggleMenu"><a>When is it</a></li>
      <li class="navigation__link" v-on:click="toggleMenu"><a>Where is it</a></li>
      <li class="navigation__link" v-on:click="toggleMenu"><a>Where can i stay</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navigation',
  data: ()=>{
    return {
      menuOpen: false
    }
  },
  methods: {
    toggleMenu: function(){
      this.menuOpen = !this.menuOpen
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  nav {
    position: fixed;
    top: 0;
    right: 0;
    z-index: 1000;
  }

  .navigation {
    position: fixed;
    top: 0;
    right: 0;
    list-style: none;
    overflow: scroll;

    @media(max-width: 850px){
      width: 100%;
      height: 100%;
      left: 100%;
      background: #e7e8f5;
      z-index: 2;
      padding-top: 100px;
      transform: translateX(0%);
      transition: transform 350ms ease-in-out;

      &--is-open {
        transform: translateX(-100%);
      }
    }

    &__link {
      display: inline-block;
      padding: 40px;
      text-transform: uppercase;
      font-size: 1.25rem;
      font-family: 'Archivo Black', sans-serif;
      cursor: pointer;
      overflow: hidden;

      @media(max-width: 850px){
        display: flex;
      }

      a {
        padding: 5px;
        position: relative;
        z-index: 2;

        &:before {
          content: '';
          position: absolute;
          height: 100%;
          width: 100%;
          background: #f5e7e7;
          left: 0;
          top: 0;
          opacity: 1;
          z-index: -1;
          transform: scaleY(0);
          transform-origin: 0;
          transition: transform 150ms ease-in-out;
        }
      }

      &:hover a {
        &:before {
          transform: scaleY(1);
        }
      }
    }

    &__toggle {
      display: none;
      @media(max-width: 850px){
        display:block;
        position: fixed;
        top: 0;
        right: 0;
        z-index: 3;
      }

      &--opened {
        display: none;
      }

      &--is-open {
        .navigation__toggle--closed {
          display: none;
        }

        .navigation__toggle--opened {
          display: block;
        }
      }

    }

  }
</style>
