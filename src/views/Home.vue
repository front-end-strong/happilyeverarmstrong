<template>
  <div class="home">
    <Hero></Hero>
    <Journey></Journey>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Journey from '@/components/Journey.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Journey
  }
}
</script>
<style lang="scss">
  .home {
    display: flex;
    flex-direction: column;
  }
</style>
