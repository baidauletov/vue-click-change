<template>
  <div class="button" :style="styles()">
    <slot></slot>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.button {
  padding: 0.5rem 1rem;
  border: 1px solid #005caf;
  border-radius: 2rem;
}
</style>
