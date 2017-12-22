<template>
  <div class="home">
    <header-content></header-content>

    <main>
      <div class="banner">
        <div class="banner__content">
          <h2>A well-being oasis</h2>
          <p>Hotel - drinks - food - music</p>
          <div class="mouse"></div>
        </div>
      </div>
    </main>

    <footer></footer>
  </div>
</template>

<script>
import HeaderContent from '@/components/HeaderContent';

export default {
  name: 'home-container',

  data() {
    return {};
  },

  components: {
    HeaderContent,
  },
};
</script>

<style lang="scss">
.banner {
  min-height: 100vh;
  position: relative;

  display: flex;
  align-items: flex-end;
  box-sizing: border-box;
  justify-content: center;

  padding-bottom: 50px;

  background: {
    image: url('../assets/img/banner.jpg');
    size: cover;
    position: center;
    repeat: no-repeat;
  }

  &__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    text-align: center;
  }

  h2 {
    margin: 0;

    font-size: 1.5em;
  }

  p {
    margin: 6px 0 24px 0;

    font-size: 0.7em;
  }

  h2,
  p {
    text-transform: uppercase;
    color: #fff;
  }

  .mouse {
    position: relative;

    width: 24px;
    height: 42px;
    border: {
      width: 2px;
      style: solid;
      color: #fff;
      radius: 15px;
    }

    &:before {
      content: '';

      position: absolute;
      top: 10%;
      right: calc(50% - 2px);

      width: 4px;
      height: 4px;
      background-color: #fff;
      border-radius: 50%;

      animation: {
        name: mouse;
        duration: 1.2s;
        iteration-count: infinite;
      }
    }
  }
}

@keyframes mouse {
  0% {
    top: 10%;
    opacity: 0;
  }
  100% {
    top: 50%;
    opacity: 1;
  }
}
</style>