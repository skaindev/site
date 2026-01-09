<template>
  <div id="layout-root">
    <AppLegalConsent />

    <div id="app-shell">
      <AppHeader />
      <Nuxt />
      <AppFooter />
    </div>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
import AppFooter from '@/components/AppFooter.vue'
import AppLegalConsent from '@/components/AppLegalConsent.vue'

export default {
  components: {
    AppHeader,
    AppFooter,
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
