<template>
  <div class="journey" id="theJourneySoFar">
    <div class="journey__container">
      <h1 class="journey__title">The<br/>Journey<br/>So <span class="journey__title--offset">Far</span></h1>
      <div class="journey__imageGrid">
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" src="@/assets/hero.jpeg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'journey',
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
.journey {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 20rem;


  &__container {
    width: 80%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: left;
    flex-direction: column;
  }

  &__title {
    width: 100%;
    color: #ffffff;
    text-align: right;
    display: block;
    font-size: 9rem;
    text-transform: uppercase;
    letter-spacing: -0.5rem;
    line-height: 7.5rem;
    position: relative;
    font-family: 'Archivo Black', sans-serif;
    z-index: 2;

    &--offset {
      display: inline-block;
      transform: translateY(100%);
    }

    @media(max-width:750px){
      margin-bottom: 30%;
      text-align: center;
      font-size: 15vw;
      letter-spacing: -1.25vw;
      line-height: 11.75vw;
    }

  }

  &__imageGrid {
    display: flex;
    flex-direction: column;
  }

  &__image {
    max-width: 100%;
    opacity: 0;
    margin-bottom: 15%;

    @media(max-width: 751px){
      margin-bottom: 20%;
    }

    @media(min-width:750px){
      max-width: 45%;

      &:nth-child(even){
        margin-left: auto;
      }
    }
  }


}
</style>
