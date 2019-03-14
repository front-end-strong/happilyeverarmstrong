<template>
  <div class="home">
    <Hero></Hero>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'

export default {
  name: 'home',
  components: {
    Hero
  }
}
</script>
<style lang="scss">
  .home {
    display: flex;
    height: 50vh;
    background: #ffffff;

    @media(max-width:700px){
      height: 80vh;
    }

  }
</style>
