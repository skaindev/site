<template>
  <div id="layout-root">
    <AppLegalConsent />

    <AppBanner />
    <AppHeader />

    <main class="main-content">
      <Nuxt />
    </main>

    <AppCopyright />
  </div>
</template>

<script>
import AppBanner from '@/components/AppBanner.vue'
import AppHeader from '@/components/AppHeader.vue'
import AppCopyright from '@/components/AppCopyright.vue'
import AppLegalConsent from '@/components/AppLegalConsent.vue'

export default {
  components: {
    AppBanner,
    AppHeader,
    AppCopyright,
    AppLegalConsent
  }
}
</script>

<style>
#layout-root {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* make page fill the viewport */
}

.main-content {
  flex: 1; /* take remaining space between header/banner and copyright */
}
</style>
