<template>
  <div class="modal" :class="{'modal--active':modalOpen}">
    <div class="modal__content">
      <h1>Change<br/>of plans</h1>
      <p>Same time, <strong>different place</strong>.<br/>Unfortunately the weather isn't looking great on Saturday, so <strong>instead of going to the Marysville Farm</strong>, you'll be going to the <strong>Narbethong Community Hall at 1:30pm for a 2pm start</strong>.</p>
      <a class="modal__button" v-on:click="closeModal">
        Got it!
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  data: ()=>{
    return {
      modalOpen: true
    }
  },
  methods: {
    closeModal: function(){
      this.modalOpen = !this.modalOpen
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/scss/colours.scss',
        '@/scss/fonts.scss';
.modal {
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.65);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10000;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background 250ms;
  color: $white;
  display: none;

  &--active {
    display: flex;
  }

  &__close {
    position: absolute;
    top: 2rem;
    right: 2rem;
    font-size: 2rem;
    color: #fff;
    font-weight: 800;
  }

  &__button {
    color: $white;
    background: $black;
    font-family: $font-bold;
    text-transform: uppercase;
    font-size: 2rem;
    padding: 2.5rem 4rem;
    margin-top: 4rem;
    display: inline-flex;
    cursor: pointer;
    transition: background 250ms, color 250ms;

    &:hover {
      background: $blue;
      color: $black;
    }

  }

  &__content {
    color: $black;
    padding: 6rem;
    background: $white;
    text-align: center;
    max-width: 700px;

    h1 {
      font-family: $font-bold;
      text-transform: uppercase;
      font-size: 6rem;
      margin-bottom: 2rem;
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

}
</style>
