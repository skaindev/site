<template>
  <div class="app">
    <AppBanner />
    <AppHeader />
    <Nuxt />
    <AppCopyright />
  </div>
</template>

<script>
import AppBanner from '@/components/AppBanner.vue'
import AppHeader from '@/components/AppHeader.vue'
import AppCopyright from '@/components/AppCopyright.vue'

export default {
  components: {
    AppBanner,
    AppHeader,
    AppCopyright
  }
}
</script>
