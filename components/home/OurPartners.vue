<template>
  <section>

  </section>
</template>

<script>
export default {
  name: 'OurPartners',
  methods: {
    goToBlog() {
      window.open('https://medium.com/Skaina-blog', '_blank')
    },
  },
}
</script>

<style lang="postcss" scoped>
@import url('../lib/media-query-helper.css');

section {
  padding: 0 0 6rem;

  @media (--viewport-small) {
    padding: 0 0 3rem;
  }
}

@media (--viewport-small) {
  .partner-logo-container {
    width: 100%;
  }

  .partner-logo-container .base-illustration {
    object-fit: cover;
    width: 100%;
  }
}
</style>
