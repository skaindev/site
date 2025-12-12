<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="Our mission"
        heading="Skaina Vision"
        class="our-mission"
      />
      <app-section-descriptor
            description="Vision: A world where no essential document, proof or record can ever disappear.
Mission: To provide a decentralized, censorship-resistant ledger capable of storing and validating information for centuries.

Skaina is not just a blockchain — it is a digital monument to truth."
style="text-align: left;" />
<div class="spc"></div>
      <app-section-descriptor
            description=" Vision: A world where no essential document, proof or record can ever disappear.
Mission: To provide a decentralized, censorship-resistant ledger capable of storing and validating information for centuries.

Skaina is not just a blockchain — it is a digital monument to truth."
style="text-align: left;" />
      <v-stack justify="space-between" wrap>
        <div
          v-for="culturePoint in culturePoints"
          :key="culturePoint.title"
          class="our-culture-points"
        >
        
          <v-blurb
            :image="culturePoint.icon"
            :alt="culturePoint.title"
            :title="culturePoint.title"
            :description="culturePoint.description"
          />
        </div>
      </v-stack>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurCulture',
  data() {
    return {
      culturePoints: [
      // {
      //     // icon: 'images/privacy.svg',
      //     // title: 'Value Privacy',
      //     // description:
      //     //   'Privacy is not a feature we build, it is a fundamental right.',
      //   },
      ],
    }
  },
}
</script>

<style lang="postcss" scoped>
@import url('../lib/media-query-helper.css');

.our-culture-points {
  width: 30%;
  justify-content: center;
  align-items: center;
  margin: 2rem 0;

  @media (--viewport-medium) {
    width: 50%;
  }
}
.description-text{
font-family: Play, Arial, Helvetica, sans-serif;
}
.our-culture-points > * {
  margin: 0 auto;
  max-width: 12rem;
}
.spc{
  padding: 1rem;
}

.spcs{
  padding: 2.4rem;
}
.our-culture-points > .blurb-description {
  font-size: 1.125rem !important;
  line-height: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1rem;
    line-height: 1.125rem;
  }
}
</style>
