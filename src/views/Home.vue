<template>
  <div class="home">
    <Hero></Hero>
    <!-- <Journey></Journey> -->
    <When></When>
    <Stay></Stay>
    <Rsvp></Rsvp>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Journey from '@/components/Journey.vue'
import Rsvp from '@/components/Rsvp.vue'
import When from '@/components/When.vue'
import Stay from '@/components/Stay.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Journey,
    When,
    Stay,
    Rsvp
  }
}
</script>
<style lang="scss">
  .home {
    display: flex;
    flex-direction: column;
  }
</style>
