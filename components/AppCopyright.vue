<template>
  <div class="app-copyright">
    <v-text font="sans" size="1rem">
      <a href="/terms/" class="link">Terms</a> © {{ currentYear }} Skaina.
    </v-text>
    <v-text font="sans" size="1rem">
      <a href="/privacy/" class="link">Privacy</a>
    </v-text>
  </div>
</template>

<script>
export default {
  name: 'AppCopyright',
  computed: {
    currentYear() {
      return new Date().getFullYear()
    },
  },
}
</script>

<style scoped>
.app-copyright {
  color: black;
  padding: 1.5rem;
  text-align: center;
  background-color: #fff;
  border-top: 1px solid #111;
}

.app-copyright .link {
  color: #3490dc;
  text-decoration: none;
  margin: 0 0.25rem;
}

.app-copyright .link:hover {
  color: #2779bd;
}
</style>
