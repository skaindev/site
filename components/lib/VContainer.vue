<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'VContainer',
}
</script>

<style lang="postcss" scoped>
@import url('./media-query-helper.css');

.container {
  color: black;
  max-width: 96rem;
  width: 80%;
  margin: 0 auto;
  background-color: #FFF;

  @media (--viewport-small) {
    width: 90% !important;
    margin: 0 auto;
  }
}
</style>
