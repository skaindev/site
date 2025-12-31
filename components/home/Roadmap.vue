<template>
  <section>
    <v-container>
      <v-stack>
        <app-section-descriptor
          title="Roadmap"
          heading="Skaina Roadmap"
          description="Discover our remarkable achievements and ongoing endeavors below. Inspired? Join us in shaping the future! Together, we can make Skaina the epitome of advancement in the realm of payments."
          style="max-width: 58rem"
        />
      </v-stack>
    </v-container>
    <div class="roadmap-container">
      <v-image
        path="images/roadmap-desktop.png"
        class="tablet-remove mobile-remove roadmap-desktop"
      />
      <div class="laptop-remove position-relative" style="text-align: center">
        <v-image path="images/roadmap-mobile-bg.png" class="roadmap-mobile" />
      </div>
    </div>
    <div class="roadmap-container">
      <a href="/tech/" target="_blank"><v-button label="See details" label-transform="uppercase" /> </a>
    </div>
  </section>
  
</template>

<script>
export default {
  name: 'Roadmap',
}
</script>

<style> 
/* Imported this for getting helper classes laptop-remove and mobile-remove */
@import url('../lib/media-query-helper.css');

section {
  margin-top: 0 !important;
  padding: 6rem 0 0;
  color: black;
  background-color: #fff;

  @media (--viewport-small) {
    padding: 3rem 0 0;
  }
}

.roadmap-container {
  margin-top: 6rem;
  text-align: center;

  @media (--viewport-medium) {
    margin-top: 3rem;
  }
}

.roadmap-desktop {
  display: none !important;
  width: 100%;
  max-width: 1720px;
}

.roadmap-mobile {
  width: 100%;
  max-width: 375px;
}
</style>
