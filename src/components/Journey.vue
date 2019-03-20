<template>
  <div class="journey" id="theJourneySoFar">
    <div class="container">
      <h1 class="title">The<br/>Journey<br/>So <span class="title--offset">Far</span></h1>
      <div class="journey__imageGrid">
        <img class="journey__image" alt="" src="@/assets/photo-1.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-2.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-3.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-4.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-5a.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-5b.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-5c.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-5d.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-7.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-7a.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-7c.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-7d.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-7e.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8a.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8b.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8c.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8d.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8e.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-8f.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
        <img class="journey__image" alt="" src="@/assets/photo-9.jpg" laxxx-opacity="(vh*0.5) 1, (vh*0.75) 0" laxxx-anchor="self"/>
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
@import '@/scss/colours.scss',
        '@/scss/fonts.scss',
        '@/scss/title.scss',
        '@/scss/container.scss',
        '@/scss/mixins.scss';

.journey {
  @extend %sectionPadded;
  padding-top: 0;
  margin-bottom: 5rem;

  &__imageGrid {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  &__image {
    max-width: 100%;
    align-self: center;
    opacity: 0;
    margin-bottom: -20%;
    width: 100%;

    @media(max-width: 751px){
      margin-bottom: 20%;
    }

    @media(min-width:750px){
      max-width: 60%;
      margin-right: auto;

      &:nth-child(even){
        margin-left: auto;
        margin-right: inherit;
      }
    }
  }
}

.title {
  text-align: right;
  &--offset {
    transform: translateY(100%);
  }
  @media(max-width:750px){
    margin-bottom: 30%;
    text-align: center;
  }
}

.container {
  width: 80%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: left;
  flex-direction: column;
}

</style>
