<template>
  <header class="app-header">
    <v-header
      logo="images/logo.svg"
  :menu-items="menuItems"
  logo-width="180"

    />

      <div class="hero">

  </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      headerCta: {
        label: 'Start Building',
        link: process.env.skainaDashboardUrl,
      },
      menuItems: [
        
      {
          name: 'About',
          link: '/about/',
        },
      // {
      //     name: 'Asknio',
      //     link: 'https://asknio.com',
      //     external: true,
      //   },
 
        //     {
        //   name: 'NioDEX',
        //   link: 'https://dex.skaina.com',
        //   external: true,
        // },
        {
          name: 'Discord',
          link: 'https://discord.gg/64wUyf78fN',
          external: true,
        },
        
        // {
        //   name: 'Roadmap',
        //   link: '/tech/',
        // },
        {
           name: 'Github',
           link: 'https://github.com/skaindev',
           external: true,
         },

              {
          name: 'Twitter',
          link: 'https://x.com/skaina',
          external: true,
        },
        
        {
          name: 'Whitepaper',
          link: 'https://skaina.com/whitepaper.pdf',
          external: true,
        },
      ],
    }
  },
}
</script>

<style scoped>
.app-header {
  position: sticky;
  top: 0;
  z-index: 100;
  color: black;
  background-color: #fff;
  height: 3.5rem;
  align-items: center;
  border-bottom: 1px solid #ccc;

.header-container img {
  width: 180px;
  height: auto;
 
}



.app-header img {
  max-height: 100%;
  width: auto;
   border-bottom: 1px solid #ccc;
}

  
}
</style>
