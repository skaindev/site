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
        {
           name: 'Github',
           link: 'https://github.com/skaindev',
           external: true,
         },
        {
          name: 'X.com',
          link: 'https://x.com/SkainaTek',
          external: true,
        },
        

      ],
    }
  },
}
</script>

<style>
.app-header {
  position: sticky;
  top: 0;
  z-index: 100;
  color: black;
  background-color: #fff;
  height: 3.5rem;
  align-items: center;
  border-bottom: 1px solid #111;
  padding: 0.5rem 0;

.header-container img {
  width: 180px;
  height: auto;
 
}

.app-header img {
  max-height: 100%;
  width: auto;
}

  
}
</style>
