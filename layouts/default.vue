<template>
  <div id="layout-root">
    <AppLegalConsent />

    <AppBanner />
    <AppHeader />

    <Nuxt />

    <!-- <AppFooter /> -->
    <AppCopyright />
  </div>
</template>

<script>
import AppBanner from '@/components/AppBanner.vue'
import AppHeader from '@/components/AppHeader.vue'
// import AppFooter from '@/components/AppFooter.vue'
import AppCopyright from '@/components/AppCopyright.vue'
import AppLegalConsent from '@/components/AppLegalConsent.vue'

export default {
  components: {
    AppBanner,
    AppHeader,
    // AppFooter,
    AppCopyright,
    AppLegalConsent
  }
}
</script>


<style>

#layout-root {
  position: static;
}

#app-shell {
  position: relative;
}
</style>
