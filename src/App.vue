<template>
  <div id="app">
    <div class="main">
      <div class="info">
        <span v-if="counter" class="info__counter">{{ counter }}</span>
        <img alt="Vue logo" src="./assets/logo.png" />
      </div>
      <vBtn class="main__button" @click="counterIncrement">Кликни меня</vBtn>
      <div class="casts">
        <div class="casts__item">
          <vTransition :toggle="counter === 1" />
        </div>
        <div class="casts__item"></div>
        <div class="casts__item"></div>
        <div class="casts__item"></div>
      </div>
    </div>
  </div>
</template>

<script>
import vBtn from "./components/ui/vBtn.vue";
import vTransition from "./components/casts/v-transition.vue";

export default {
  name: "App",
  components: {
    vBtn,
    vTransition,
  },
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    counterIncrement() {
      this.counter++;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 3rem;
}
.info {
  position: relative;
  width: 100%;
  &__counter {
    position: absolute;
    top: 0;
    left: 0;
  }
}
.casts {
  display: grid;
  gap: 2rem;
  grid-template-columns: repeat(4, 1fr);
  width: 100%;
  padding-top: 3rem;
  &__item {
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid #2c3e50;
    border-radius: 1rem;
    width: 100%;
    min-height: 15rem;
  }
}
</style>
