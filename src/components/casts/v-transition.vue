<template>
  <transition name="fade">
    <p class="v-transition" v-if="toggle">
      <a
        class="v-transition__item"
        href="https://ru.vuejs.org/v2/guide/transitions.html"
        target="blank"
      >
        transition
      </a>
      <a
        class="v-transition__item"
        href="https://ru.vuejs.org/v2/guide/conditional.html"
        target="blank"
      >
        v-if
      </a>
    </p>
  </transition>
</template>

<script>
export default {
  props: {
    toggle: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss">
.v-transition {
  display: flex;
  flex-direction: column;
  justify-self: center;
  align-items: center;
  &__item {
    font-size: 1rem;
    padding: 1rem;
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
