<template>
  <ul class="navigation">
    <li><a>When is it</a></li>
    <li><a>Where is it</a></li>
    <li><a>Where to stay</a></li>
  </ul>
</template>

<script>
export default {
  name: 'Navigation'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .navigation {
    position: fixed;
    top: 0;
    right: 0;
    list-style: none;

    li {
      display: inline-block;
      padding: 40px;
      text-transform: uppercase;
      font-size: 1.25rem;
      font-family: 'Archivo Black', sans-serif;
      cursor: pointer;
      overflow: hidden;

      a {
        padding: 5px;
        position: relative;
        z-index: 2;

        &:before {
          content: '';
          position: absolute;
          height: 100%;
          width: 100%;
          background: #f5e7e7;
          left: 0;
          top: 0;
          opacity: 1;
          z-index: -1;
          transform: scaleY(0);
          transform-origin: 0;
          transition: transform 150ms ease-in-out;
        }
      }


      &.is-active,
      &:hover a {
        &:before {
          transform: scaleY(1);
        }
      }


    }
  }
</style>
