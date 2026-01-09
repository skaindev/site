<template>
  <div id="layout-root">
    <AppLegalConsent />

    <div id="app-shell">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import AppLegalConsent from '@/components/AppLegalConsent.vue'

export default {
  components: {
    AppLegalConsent
  }
}
</script>
