<template>
  <div class="when" id="whenIsIt">
    <div class="container">
      <h1 class="title">When<br/>AND <span class="title--offset">where</span></h1>

      <div class="when__location">
        <figure class="when__hero">
          <img src="@/assets/locations/marysville-farm-house.jpg"/>
          <figcaption>
            <h2>MARYSVILLE<br/><span>COUNTRY</span><br/>FARM</h2>
          </figcaption>
        </figure>

        <div class="when__content">
          <p>700 metres from Marysville town centre is this beautiful family farm. Surrounded by nothing by cows, orchard and forest the farm is the perfect place for us to share our vows and love together.</p>
          <a class="cta" href="https://goo.gl/maps/tUgSKtaXAzJ2" target="blank">View the map</a>
        </div>
      </div>

      <div class="when__location when__location--right">
        <figure class="when__hero">
          <img src="@/assets/locations/narbethong-community-hall.jpg"/>
          <figcaption>
            <h2>NARBETHONG<br/><span>COMMUNITY</span><br/>HALL</h2>
          </figcaption>
        </figure>

        <div class="when__content">
          <p>Situated at north of the Black Spur and in the heart of the Yarra Valley is <strong>Narbethong Community Hall</strong>. After burning down during the black saturday fires the space presented an opportunity to bring new life and typology to the area, as well as creating a space that celebrates the history and uniqueness of Narbethong.</p>
          <a class="cta" href="https://goo.gl/maps/BRzXncf8v1B2" target="blank">View the map</a>
        </div>
      </div>

      <div class="when__date">
        <h2>November<br/>2nd<br/><span class="when__date--offset">2019</span></h2>
      </div>

    </div>
  </div>
</template>

<script>

export default {
  name: 'When'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/scss/colours.scss',
        '@/scss/fonts.scss',
        '@/scss/title.scss',
        '@/scss/container.scss',
        '@/scss/cta.scss',
        '@/scss/mixins.scss';

.when {
  @extend %section;
  background: $white;
  position: relative;

  &__location {
    &:last-child{
      margin-top: 8rem;
    }

    &--right {
      .when__hero {
        margin-right: auto;
        margin-left: inherit;
      }

      .when__content {
        margin-right: inherit;
        margin-left: auto;
      }

      figcaption {
        h2 {
          font-family: $font-bold;
          position: absolute;
          bottom: 5%;
          left: 5%;
          color: #ffffff;
          text-align: left;
        }
      }
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
      h2 {
        font-family: $font-bold;
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

  &__content {
    width: 60%;
    text-align: left;
    margin-right: auto;
    padding: 10rem 0;
    color: $black;

    @media(max-width: 750px){
      width: 100%;
    }

    p {
      font-size: 21px;
      font-weight: 500;
      line-height: 1.75;
      letter-spacing: -0.0014rem;

      strong {
        font-weight: 600;
      }
    }
  }

  &__date {
    width: 100%;
    font-family: $font-bold;
    font-size: 4vw;
    text-align: left;
    line-height: 0.8;

    @media(max-width: 750px){
      font-size: 7vw;
    }

    &--offset {
      display: inline-block;
      transform: translateX(50%)
    }
  }

  .addeventatc {
    margin-top: 8rem;
  }

}

.title {
  color: #e7e8f5;
  text-align: left;
  &--offset {
    transform: translateX(40%);
    @media(min-width:751px){
      transform: translateX(-40%) translateY(100%);
    }
  }
}

</style>
