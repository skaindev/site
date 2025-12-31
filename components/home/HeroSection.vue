<template>
  <section class="hero-section">
    <v-container>
      <v-stack
        justify="space-between"
        md-direction="column-reverse"
        md-align="center"
        class="position-relative"
      >
        <v-stack direction="column" class="hero-content-container">
          <v-heading :level="1" class="hero-title">
            <div>Your Legacy. Your Way. Forever.</div>            
          </v-heading>
          <v-stack direction="column">
            <app-section-descriptor
              description="Skaina is a next-generation blockchain designed to preserve what truly matters: documents, patents, proofs, records, and digital assets that must never be lost, altered, or destroyed.
               Built for permanence. Engineered for truth. Powered by a decentralized network that protects your legacy — forever."
              class="hero-description"
            />
            <v-stack align="center" gap="1.5rem" sm-gap="1rem" wrap>
              <router-link to="">
                <v-button label="WHITEPAPER" label-transform="uppercase" />
              </router-link>
              <router-link to="">
                <v-button
                  color="#000"
                  variant="outline"
                  label="DISCORD"
                  label-transform="uppercase"
                  class="secondary-button"
                />
              </router-link>
            </v-stack>
          </v-stack>
        </v-stack>
        <v-image
              class="hero-image"
              path="images/globe-chain.png"
            />     
      </v-stack>
    </v-container>
  </section>  
</template>
<script>
const skainaUrl = process.env.skainaBookDemoUrl
const skainaDashboardUrl = process.env.skainaDashboardUrl

export default {
  name: 'HeroSection',
  data() {
    return {
      isIntroPlaying: false,
      skainaUrl,
      skainaDashboardUrl,     
    }
  },

}
</script>

<style>
@import url('../lib/media-query-helper.css');

.hero-section {
  padding: 0 0 5rem !important;
  margin-top: 6rem !important;


  @media (--viewport-small) {
    padding: 10px 0 !important;
    margin-top: 0 !important;
  }
}

.hero-image {
  max-width: 36rem;
  width: 100%;



  @media (--viewport-medium) {
    margin-right: 0;
  }

  @media (--viewport-small) {
    margin-top: 2rem;
  }
}

.hero-description {
  font-family: 'Prosto One', sans-serif;
  margin-block: 2rem;
}

.hero-content-container {
  font-family: 'Prosto One', sans-serif;
  max-width: 40rem !important;
  margin-top: 4rem !important;
}

.hero-title {
  font-family: 'Prosto One', sans-serif;
  margin-block: 0;
  max-width: 30ch;
}
</style>
