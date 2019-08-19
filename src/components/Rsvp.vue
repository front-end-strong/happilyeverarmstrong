<template>
  <div class="rsvp" id="rsvp">
    <div class="rsvp__content container">
      <h1 class="rsvp__title title">RSVP<br/>TO ME</h1>

      <div class="rsvp__copy">
        <p>We can't wait to celebrate with you! To RSVP send Josh a message with your attendence and any dietry requirements on:</p>
        <h2>0420 316 953</h2>
      </div>

    </div>
  </div>
</template>

<script>

export default {
  name: 'rsvp',
  mounted(){
    window.onload = function() {
    	laxxx.setup({ /* opts */ }) // init
    	document.addEventListener('scroll', function(e) {
    	  laxxx.update(window.scrollY) // update every scroll
    	}, false)
    	laxxx.update(window.scrollY) // set initial positions
    }
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

.rsvp {
  @extend %sectionPadded;
  background: $white;

  .title {
    color: $blue;
    transform: translateY(-6rem);
  }

  &__content {
    color: $black;
    margin: 4rem 0 3rem;

    p {
      font-size: 21px;
      font-weight: 500;
      line-height: 1.25;
      letter-spacing: -0.0014rem;
      text-align: center;

      strong {
        font-weight: 600;
      }
    }

    h2 {
      font-family: $font-bold;
      font-size: 8rem;
      // font-weight: 500;
      line-height: 1.75;
      letter-spacing: -0.0014rem;
      text-align: center;
      margin-top: -2rem;

      strong {
        font-weight: 600;
      }
    }

  }

  &__copy {
    width: 100%;
    max-width: 680px;

    @media(max-width: 780px){
      width: 100%;
      max-width: 100%;

      h2 {
        font-size: 3rem;
        margin-top: 0;
      }
    }

  }

}

</style>
