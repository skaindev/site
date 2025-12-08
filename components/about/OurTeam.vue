<template>
  <section style="margin-bottom: 10rem">
    <v-container>
      <v-stack justify="space-between">
        <app-section-descriptor
          title="The Developers"
          heading="Skaina Builders"
        />
      </v-stack>
      <v-stack
        justify="space-between"
        md-direction="column"
        class="member-container"
        wrap
      >
      
      <app-section-descriptor
            description="Skaina team consists of a group of software engineers and designers which are passionate about blockchain technology and cryptocurrencies in general, with a strong belief in the freedom and privacy of each individual.

Our team is a perfect blend of core developers and UX/UI designers. Find out more about Skaina project by reading the Whitepaper."
style="text-align: left;" />
        
      </v-stack>


      
      <div class="spcs"></div>
      <app-section-descriptor
        title="Our mission"
        heading="Skaina Vision"
        style="max-width: 60rem"
      />
      <app-section-descriptor
            description="With Skaina, users can expect lightning-fast transaction speeds, eliminating the frustrating delays that have long been associated with traditional payment systems. 
            Our platform ensures that transactions are processed swiftly, enabling seamless and timely transfers of value."
style="text-align: left;" />
<div class="spc"></div>
      <app-section-descriptor
            description="       Our mission at Skaina is to revolutionize traditional payments. By leveraging cutting-edge blockchain technology, 
        we offer lightning-fast transactions, enhanced security, heightened privacy, and significant cost savings. Join us in reshaping the future of payments, making it accessible, secure, and efficient for everyone. 
        Together, let's unlock the transformative power of decentralization."
style="text-align: left;" />

    </v-container>


  </section>
</template>

<script>
export default {
  name: 'OurTeam',
  data() {
    return {

    }
  },
}
</script>

<style lang="postcss" scoped>
@import url('../lib/media-query-helper.css');
.member-container {
  margin: 1rem 0;
  text-align: center;
  @media (--viewport-medium) {
    text-align: start;
  }
}

.member-container > * {
  margin: 1rem 0;
  flex: 1 0 33%;
}
.other-members {
  max-height: 0;
  opacity: 0;
  overflow: hidden;
  transition: max-height 0.4s, opacity 0.8s;
}
.spc{
  padding: 1rem;
}
.spcs{
  padding: 2.4rem;
}
.expanded {
  opacity: 1;
  max-height: 100%;
}
@media (--viewport-medium) {
  .member-container > * + * {
    margin-top: 1rem;
  }
}
</style>