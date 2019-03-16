<template>
  <div class="stay" id="whereCanIStay">
    <div class="container">
      <h1 class="title">Where<br/>can<br/>I<span class="title--offset">stay</span></h1>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Stay',
  mounted(){
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/scss/colours.scss',
        '@/scss/fonts.scss',
        '@/scss/title.scss',
        '@/scss/container.scss',
        '@/scss/mixins.scss';

.stay {
  @extend %section;
}

.title {
  color: $white;
  text-align: right;

  &--offset {
    // @media(min-width:751px){
      transform: translateX(-0%) translateY(100%);
    // }
  }

  @media(max-width:750px){
    text-align: center;
  }
}

</style>
