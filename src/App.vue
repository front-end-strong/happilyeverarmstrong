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

$font-bold: 'Archivo Black', sans-serif;

* {
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html,body {
  min-height: 100vh;
  background: #f5e7e7;
  color: #2c3e50;
  font-family: 'Montserrat', sans-serif;
  font-weight: 100;
  font-size: 10px;
}

strong {
  font-weight: 100;
}


</style>
