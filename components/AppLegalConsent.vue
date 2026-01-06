<template>
  <client-only>
    <div v-if="show" class="legal-banner">
      <div class="legal-content">
        <p>
          By using this website, you agree to our
          <NuxtLink to="/terms">Terms & Conditions</NuxtLink>
          and
          <NuxtLink to="/privacy">Privacy Policy</NuxtLink>.
        </p>
        <button class="legal-btn" @click="accept">Accept</button>
      </div>
    </div>
  </client-only>
</template>


<script>
export default {
  name: 'AppLegalConsent',
  data() {
    return {
      show: false
    }
  },
  mounted() {
    const accepted = localStorage.getItem('skaina_legal_accepted')
    if (!accepted) {
      this.show = true
    }
  },
  methods: {
    accept() {
      localStorage.setItem('skaina_legal_accepted', 'true')
      this.show = false
    }
  }
}
</script>

<style scoped>
.legal-banner {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #0a0a0a;
  color: #fff;
  z-index: 9999;
  padding: 1rem;
}

.legal-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  gap: 1rem;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.legal-content a {
  color: #4da3ff;
  text-decoration: underline;
}

.legal-btn {
  background: #4da3ff;
  border: none;
  color: #000;
  padding: 0.5rem 1.25rem;
  border-radius: 4px;
  cursor: pointer;
  font-weight: 600;
}

.legal-btn:hover {
  opacity: 0.9;
}
</style>
