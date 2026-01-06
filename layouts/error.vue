<template>
  <div>
    <AppHeader />
    <Nuxt />
    <AppFooter />
    <AppLegalConsent />
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
