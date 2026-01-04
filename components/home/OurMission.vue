<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="CONTACT"
        heading="Get In Touch"
        style="max-width: 60rem"
      />

      <app-section-descriptor
            description="Email: hello@skaina.com"
style="text-align: left;" />
<div class="spc"></div>

      <app-section-descriptor
            description="Skaina is more than a blockchain — it is a digital vault for humanity’s most valuable information.
A platform where truth is permanent, documents live forever, and legacy becomes unbreakable."
style="text-align: left;" />
<div class="spc"></div>



<app-section-descriptor
            description="Security is also at the core of our mission. Traditional payment methods have often fallen victim to security breaches and data theft, exposing individuals and businesses to significant risks. Skaina tackles this challenge head-on by implementing robust security measures, leveraging the immutability and transparency of blockchain technology. Our users can have peace of mind, knowing that their transactions are protected by state-of-the-art cryptographic protocols and secure decentralized networks."
style="text-align: left;" />
<div class="spc"></div>

<app-section-descriptor
            description="Privacy is another aspect we prioritize. We understand the importance of personal and financial privacy in an increasingly interconnected world. Skaina empowers individuals and businesses to maintain their privacy by minimizing the collection and exposure of sensitive data. Through our platform, users can conduct transactions with confidence, knowing that their personal information is safeguarded."
style="text-align: left;" />
<div class="spc"></div>

<app-section-descriptor
            description="Your legacy, our way. Forever."
style="text-align: left;" />
<div class="spc"></div>

      <v-stack justify="space-between" wrap>
        <div
          
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
  name: 'ContactUs',
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

section {
  @media (--viewport-small) {
    margin-top: 6 !important;
  }
}

.illustration-container {
  position: relative;
}

.illustration-container::before {
  content: '';
  position: absolute;
  inset: -20%;
  z-index: -1;
  background: radial-gradient(
    50% 40% at 50% 40%,
    rgba(248, 81, 142, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}

.principles-illustration {
  width: 100%;
  max-width: 28rem;
  align-self: center;

  @media (--viewport-medium) {
    max-width: 20rem;
    margin: 2rem auto;
  }
}
</style>
