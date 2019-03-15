<template>
  <div class="when" id="whenIsIt">
    <div class="when__container">
      <h1 class="when__title">When<br/>AND <span class="when__title--offset">where</span></h1>
      <figure class="when__hero">
        <img src="@/assets/narbethong-community-hall.jpg"/>
        <figcaption>
          <h1>NARBETHONG<br/><span>COMMUNITY</span><br/>HALL</h1>
        </figcaption>
      </figure>
      <h2>2nd November, 2019</h2>
    </div>
  </div>
</template>

<script>

export default {
  name: 'When',
  mounted(){
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.when {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 20rem;
  padding: 20rem 0;
  background: #ffffff;

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
    color: #e7e8f5;
    text-align: left;
    display: block;
    font-size: 9rem;
    text-transform: uppercase;
    letter-spacing: -0.5rem;
    line-height: 7.5rem;
    position: relative;
    z-index: 2;
    font-family: 'Archivo Black', sans-serif;

    &--offset {
      display: inline-block;
      @media(min-width:751px){
        transform: translateX(-40%) translateY(100%);
      }
    }

    @media(max-width:750px){
      margin-bottom: 30%;
      text-align: center;
      font-size: 15vw;
      letter-spacing: -1.25vw;
      line-height: 11.75vw;
    }

  }

  &__hero {
    width: 87%;
    margin-left: auto;
    margin-top: -2.5%;
    position: relative;

    @media(max-width:750px){
      width: 100%;
    }

    figcaption {
      h1 {
        font-family: 'Archivo Black', sans-serif;
        position: absolute;
        bottom: 5%;
        right: 5%;
        color: #ffffff;
        text-align: left;

        span {
          display: inline-block;
          transform: translateX(20%);
        }


        @media(min-width:751px){
          font-size: 3rem;
          letter-spacing: -0.1rem;
          line-height: 2.75rem;
        }

        @media(min-width:1300px){
          font-size: 6rem;
          letter-spacing: -0.3rem;
          line-height: 4.75rem;
        }

      }
    }

    img {
      width: 100%;
    }

  }

}
</style>
