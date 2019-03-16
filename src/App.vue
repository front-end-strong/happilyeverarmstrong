<template>
  <div id="app">
    <Navigation></Navigation>
    <router-view/>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue'

export default {
  name: 'app',
  components: {
    Navigation
  }
}
</script>


<style lang="scss">
@import '@/scss/colours.scss',
        '@/scss/fonts.scss';

* {
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html,body {
  min-height: 100vh;
  background: $pink;
  color: $black;
  font-weight: 100;
  font-size: 10px;
  font-family: $font-body;
}

strong {
  font-weight: 100;
}


</style>
