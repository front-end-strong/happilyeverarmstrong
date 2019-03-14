<template>
  <div class="hero">
    <div class="hero__container">
      <h1>
        <span>#</span>Happily<wbr><span>Ever</span><wbr>Armstrong<br/><strong>2019</strong>
      </h1>
      <!-- <img src="@/assets/hero.jpeg"/> -->
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
  .hero {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;

    &__container {
      width: 80%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;

      h1 {
        text-align: left;
        font-size: 4rem;
        font-weight: 300;
        position: relative;

        strong {
          font-size: 6rem;
          opacity: 0.5;
        }

      }

      img {
        width: 700px;
        margin: 12.5%;
        transform: rotate(-4deg);
        transition: transform 250ms ease-out, filter 250ms ease-out;
        filter: drop-shadow(0 0 20px rgba(0,0,0,0.65));
        // box-shadow: 16px 16px 20px black;

        &:hover {
          transform: scale(1.25) rotate(4deg);
          filter: drop-shadow(0 0 60px rgba(0,0,0,0.25));
        }
      }

    }
  }
</style>
