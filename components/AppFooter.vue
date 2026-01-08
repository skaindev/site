<template>
  <footer>
    <v-container class="footer-container"  >
      <v-stack
        align="center"
        justify="space-around"
        :grow="1"
        class="footer-logo-container"
      >     
      </v-stack>
         <app-section-descriptor
        title="Contact"
        class="get-in"
        heading="GET IN TOUCH"
      
        style="max-width: 64rem"
      />
      <v-stack
        justify="space-between"
        md-direction="column"
        md-align="center"
        class="footer-navigation-container"
      >

        <v-stack direction="column">
          <v-text font="sans" :weight="600" class="get-in-touch">
              Email:
            </v-text>
          <a href="mailto:hello@skaina.com">
            <v-text font="sans" :weight="400" class="footer-mailing">
              hello@skaina.com
            </v-text>
          </a>
         
          <v-stack style="margin-top: 3rem" md-justify="space-evenly">
            <a href="https://twitter.com/Skaina_net" target="_blank">
              <v-image
                path="images/social/twitter.png"
                class="footer-social-link"
                alt="Skaina Twitter"
              />
            </a>

            <a
              style="margin-left: 2rem"
              href="https://discord.skaina.com"
              target="_blank"
            >
              <v-image
                path="images/social/discord.png"
                class="footer-social-link"
                alt="Skaina Discord"
              />
            </a>
            <a
              style="margin-left: 2rem"
              href="https://t.me/Skaina_net"
              target="_blank"
            >
              <v-image
                style="height: 44px; width: auto;"
                path="images/social/telegram.png"
                class="footer-social-link"
                alt="Skaina Telegram"
              />
            </a>
            <a
              style="margin-left: 2rem"
              href="https://github.com/Skaina-net"
              target="_blank"
            >
              <v-image
                style="height: 44px; width: auto;"
                path="images/social/github.png"
                class="footer-social-link"
                alt="Skaina Github"
              />
            </a>

          </v-stack>
 
        </v-stack>

        <!-- Footer Links -->
         <v-stack
          class="footer-links-container"
          justify="space-between"
          :grow="1"
        >

          <v-stack direction="column" class="footer-links">
            <!-- <a href=""><v-text></v-text></a>
            <a href="/about/"><v-text>About</v-text></a>
            <a href="https://blog.skaina.com"><v-text>Blogger</v-text></a> -->
            <!-- <a href="/careers/"><v-text>Careers</v-text></a> -->

          </v-stack>
              <v-image class="footer-orbs" path="images/footer-orbs.svg" />
  
        </v-stack> 
      </v-stack>
    </v-container>
  </footer>
</template>

<script>
const skainaDiscordUrl = process.env.skainaDiscordUrl
const skainaBookDemoUrl = process.env.skainaBookDemoUrl

export default {
  name: 'AppFooter',
  data() {
    return {
      skainaDiscordUrl,
      skainaBookDemoUrl,
    }
  },
}
</script>

<style lang="css" scoped>
@import url('./lib/media-query-helper.css');

footer {
  color: #000;
  background-color: #fff;
  background-size: cover;
  overflow-x: hidden;
  border-bottom: 1px solid #ccc;

  @media (--viewport-small) {
    background-color: #000;
    background-size: 100%;
  }
}

.footer-logo-container {
  padding: 0;
  position: relative;

  @media (--viewport-small) {
    padding: 0;
  }
}

.footer-logo {
  margin: 0 auto;
  width: 8rem;
  height: auto;

  @media (--viewport-medium) {
    width: 6rem;
  }
}

.footer-navigation-container {
  padding: 4rem 0;

  @media (--viewport-small) {
    padding: 2rem 0;
  }
}

.footer-links-container {
  max-width: 100%;

  @media (--viewport-medium) {
    width: 100%;
    margin-top: 2rem;
    max-width: unset;
  }
}

.footer-links > * + * {
  margin-top: 3rem;
}

.footer-social-link {
  width: 3rem;
}

a {
  text-decoration: none;
}

.footer-orbs {
  max-width: 48rem;
  margin-top: -10rem;
  
}

.footer-links a * {
  font-family: var(--font-sans);
  font-weight: 500;
  font-size: 1.25rem;
  line-height: 0.5rem;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 0.5rem;
  }
}

.footer-mailing {
  color: #000;
  font-size: 1.5rem;
  line-height: 2.25rem;
}

/* .get-in {
  margin-top: 2rem;
} */
.get-in-touch {
  font-size: 1.5rem;
  line-height: 2.25rem;
  color: #272727;


  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}

@media (--viewport-small) {
  .footer-logo-container > *:first-child {
    width: 40%;
  }

  .footer-logo-container > *:last-child {
    width: 150%;
  }
}

.book-demo-container {
  margin-top: 4rem;
}

.footer-container{
  margin-bottom: 2rem;
}

.book-demo-description {
  max-width: 21rem;
  line-height: 1.5;
}

.book-demo-btn {
  width: 14rem;
  height: 3.25rem;
  margin-top: 2rem;
}
</style>
