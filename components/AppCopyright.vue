<template>
  <div class="app-copyright">
    <v-text font="sans" size="1rem">
      <a href="/terms/" class="link">Terms</a>
      <span class="separator">© {{ currentYear }} Skaina.</span>
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
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.5rem;
  background-color: #fff;
  border-top: 1px solid #111;
  color: black;
  font-size: 1rem;
  gap: 0.5rem; /* spacing between links and text */
}

.app-copyright .link {
  color: #888;
  text-decoration: none;
}

.app-copyright .link:hover {
  color: #444;
}

.app-copyright .separator {
  margin: 0 0.25rem;
}
</style>
