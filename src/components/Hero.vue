<template>
  <div class="hero">
    <div class="hero__container">
      <h1>
        <span>#</span>Happily<wbr><span>Ever</span><wbr>Armstrong<br/><strong>2019</strong>
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hero'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/scss/colours.scss',
        '@/scss/fonts.scss';

  .hero {
    width: 100%;
    height: 50vh;
    display: flex;
    background: #ffffff;
    justify-content: center;

    @media(max-width:700px){
      height: 80vh;
    }


    &__container {
      width: 80%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: left;

      @media(max-width:800px){
        justify-content: center;
      }

      h1 {
        text-align: left;
        font-size: 5.25rem;
        font-weight: 300;
        position: relative;

        @media(min-width: 801px){
          // transform: translateX(-50%);
        }

        @media(max-width:800px){
          font-size: 6vw;
          text-align: center;
        }

        strong {
          position: absolute;
          top: 50%;
          right: -25%;
          opacity: 0.05;
          font-size: 24rem;
          font-family: 'Archivo Black', sans-serif;
          font-weight: 100;
          transform: translateY(-50%);

          @media(max-width:800px){
            font-size: 30vw;
            text-align: center;
            left: 50%;
            right: initial;
            transform: translateX(-50%) translateY(-50%);
          }

        }
      }
    }
  }
</style>
