<template>
  <div class="when" id="whenIsIt">
    <div class="container">
      <h1 class="title">Where<br/>AND <span class="title--offset">WHEN</span></h1>

      <div class="when__location">
        <figure class="when__hero">
          <img src="@/assets/locations/narbethong-community-hall.jpg"/>
          <figcaption>
            <h2>NARBETHONG<br/><span>COMMUNITY</span><br/>HALL</h2>
          </figcaption>
        </figure>

        <div class="when__content">
          <h3>2pm<br/><strong>Ceremony</strong></h3>
          <p>
            Situated north of the Black Spur and in the heart of the Yarra Valley is Narbethong Community Hall. After burning down during the black saturday fires the space presented an opportunity to bring new life and typology to the area, as well as creating a space that celebrates the history and uniqueness of Narbethong.<br/><br/>
            It's here where our ceremony will take place. After the ceremony the hall will be reset, which will give you a chance to rest and recharge. Head back to your hotel or hang out at the Narby pub whilst we get the hall ready for the reception.<br/><br/>
            <strong>606 Maroondah Hwy, Narbethong</strong></p>
          <a class="cta" href="https://goo.gl/maps/BRzXncf8v1B2" target="blank">View the map</a>
        </div>
      </div>

      <div class="when__location when__location--right">


        <div class="when__content">
          <h3>6pm<br/><strong>Reception</strong></h3>
          <p>
            After you've had some time to relax, gear up and meet us back at the Narbethong Community Hall. There will be drinks and charcuterie upon arrival, so grab a drink - mingle and get comfortable as the bridal party will be joining you soon for a fantastic night!
            <br/><br/>
            <strong>606 Maroondah Hwy, Narbethong</strong><br/>
          </p>
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
        text-align: right;
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
    padding: 10rem 0 0;
    color: $black;

    @media(max-width: 750px){
      width: 100%;
    }

    h3 {
      font-size: 5rem;
      font-weight: 900;
      line-height: 1;
      margin-bottom: 3rem;
      strong {
        font-weight: 300;
      }
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
  color: $blue;
  text-align: left;
  &--offset {
    transform: translateX(40%);
    @media(min-width:751px){
      transform: translateX(-40%) translateY(100%);
    }
  }
}

</style>
