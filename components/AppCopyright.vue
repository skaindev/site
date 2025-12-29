<template>
  <div>
    <v-text font="sans" size="1rem" >
      <a href="/terms/"
              >
    <v-text size="1rem" >Terms</v-text></a
            >
      © {{ currentYear }} Skaina.
    </v-text>
        <v-text font="sans" size="1rem" >
      <a href="/terms/"
              >
    <v-text size="1rem" >Privacy.</v-text></a
            >
    
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

<style lang="css" scoped>
div {
  color: black;
  padding: 1.5rem;
  text-align: center;
  background-color: #FFF;
  border-top: 1px solid #111;
}
</style>
