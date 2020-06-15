<template>
  <button class="button" @click="$emit('click')">
    <slot></slot>
  </button>
</template>

<script>
export default {};
</script>

<style lang="scss">
.button {
  cursor: pointer;
  width: fit-content;
  height: fit-content;
  color: white;
  font-size: 0.9rem;
  letter-spacing: 0.07rem;
  text-transform: uppercase;
  transition: 0.3s;
  border: 1px solid #005caf;
  border-radius: 2rem;
  padding: 0.7rem 1.2rem;
  background: #005caf;
  box-shadow: 0 3px 1px -2px rgba(0, 0, 0, 0.2), 0 2px 2px 0 rgba(0, 0, 0, 0.14),
    0 1px 5px 0 rgba(0, 0, 0, 0.12) !important;
  &:hover {
    background: rgba(#005caf, 0.8);
  }
  outline: none;
}
</style>
