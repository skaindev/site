<template>
  <div class="banner">
    <v-text line-height="1.5" :weight="500" size="1rem">
      <a href="https://testnet.skaina.com" target="_blank">Testnet will go live Q1 2026!</a>
    </v-text>
  </div>
  
</template>

<style lang="css" scoped>
@import url('./lib/media-query-helper.css');

.banner {
  /* display: none; */
  background: #000; 
  padding: 0.25em 1.5em;
  color: #FFF;
  text-align: center;
  @media (--viewport-small) {
    padding: 0.25rem 2rem;
  }
}

a {
  color: var( --color-white);
  transition: opacity 0.4s ease-in;
  opacity: 1;
  text-underline-offset: 0.1em;
}

a:hover,
a:focus {
  opacity: 0.8;
  transition: opacity 0.4s ease-in;
}
</style>
