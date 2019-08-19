<template>
  <div class="runsheet" id="runsheet">
    <div class="runsheet__container">
      <h1 class="title">THE<br/><span class="title--offset">RUN</span><br/>SHEET</h1>
      <div class="runsheet__content">
        <h2><strong>2pm</strong><br/>The Ceremony</h2>
        <p>700 metres from Marysville town centre is this beautiful family farm. Surrounded by nothing by cows, orchard and forest the farm is the perfect place for us to share our vows and love together.</p>
      </div>

      <div class="runsheet__content">
        <h2><strong>6pm</strong><br/>The Reception</h2>
        <p>700 metres from Marysville town centre is this beautiful family farm. Surrounded by nothing by cows, orchard and forest the farm is the perfect place for us to share our vows and love together.</p>
      </div>

    </div>
  </div>
</template>

<script>

export default {
  name: 'runsheet',
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

.runsheet {
  @extend %section;
  padding: 20rem 0;

  &__container {
    width: 80%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: left;
    flex-direction: column;
  }

  &__content {
    width: 100%;
    display: flex;
    flex-direction: column;

    &:not(:last-child){
      margin-bottom: 10rem;
    }

    &:nth-child(odd){
      align-items: flex-end;
      text-align: right;
    }

    h2 {
      font-size: 5rem;
      font-weight: 300;
      margin-bottom: 5rem;
      strong {
        font-weight: 900;
      }
    }

    p {
      width: 60%;
      font-size: 21px;
      font-weight: 500;
      line-height: 1.75;
      letter-spacing: -0.0014rem;

      strong {
        font-weight: 600;
      }
    }

  }

}

.title {
  text-align: right;
  color: $black;

  &--offset {
    transform: translateX(-75%);
  }

  @media(max-width:750px){
    margin-bottom: 30%;
    text-align: center;
  }
}

</style>
