<template>
  <div class="whitepaper-container">
    <!-- Sticky Table of Contents -->
    <aside class="toc">
      <h3>Table of Contents</h3>
      <ul>
        <li
          v-for="(section, index) in whitepaperSections"
          :key="index"
          :class="{ active: activeSection === index }"
        >
          <a href="#" @click.prevent="scrollToSection(index)">
            {{ section.title }}
          </a>
        </li>
      </ul>
    </aside>

    <!-- Main Whitepaper Content -->
    <main class="whitepaper-page">
      <v-heading>Skaina Whitepaper</v-heading>

      <section
        v-for="(section, index) in whitepaperSections"
        :key="index"
        :ref="'section-' + index"
        class="whitepaper-section"
      >
        <h2 class="section-title">{{ section.title }}</h2>
        <div class="section-text" v-html="section.content"></div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeSection: 0,
      whitepaperSections: [
        {
          title: "1. Abstract",
          content: `Skaina is a next-generation blockchain designed to permanently preserve information...`
        },
        {
          title: "2. Vision & Mission",
          content: `<strong>Vision:</strong> A world where no essential document can ever disappear...`
        },
        {
          title: "3. Core Principles",
          content: `<ul><li><strong>Permanence:</strong> Once stored, data cannot be removed...</li></ul>`
        },
        {
          title: "4. Architecture Overview",
          content: `Layer 1 – Core Blockchain...<br/>Layer 2 – Data Anchoring & Proof Layer...`
        },
        {
          title: "5. Consensus & Blockchain Parameters",
          content: `Consensus Engine: Tendermint Core...`
        },
        {
          title: "6. Tokenomics",
          content: `Native Token: SKA...`
        },
        {
          title: "7. Use Cases",
          content: `<ul><li>Intellectual Property...</li></ul>`
        },
        {
          title: "8. Governance Model",
          content: `Decentralized and community-driven...`
        },
        {
          title: "9. Security & Longevity",
          content: `Advanced cryptographic protections...`
        },
        {
          title: "10. Roadmap",
          content: `Phase 1 – Foundation...`
        },
        {
          title: "11. Conclusion",
          content: `Skaina is more than a blockchain — it is a digital vault...`
        }
      ]
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll, { passive: true });
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    scrollToSection(index) {
      const el = this.$refs['section-' + index][0];
      if (el) {
        window.scrollTo({
          top: el.offsetTop - 20,
          behavior: "smooth"
        });
      }
    },
    handleScroll() {
      const scrollPos = window.scrollY + 100; // offset for heading
      this.whitepaperSections.forEach((_, index) => {
        const el = this.$refs['section-' + index][0];
        if (el && el.offsetTop <= scrollPos) {
          this.activeSection = index;
        }
      });
    }
  }
};
</script>

<style scoped>
.whitepaper-container {
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  gap: 2rem;
}

.whitepaper-page {
  flex: 1;
  font-family: "Inter", sans-serif;
  line-height: 1.6;
  color: #1c1c1c;
}

.whitepaper-section + .whitepaper-section {
  margin-top: 2.5rem;
}

.section-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #111;
}

.section-text {
  font-size: 1rem;
  color: #333;
}



/* Sticky Table of Contents */
.toc {
  flex: 0 0 250px;
  position: sticky;
  top: 2rem;
  align-self: flex-start;
  background: #f9f9f9;
  padding: 1rem;
  border-radius: 8px;
  border: 1px solid #ddd;
  height: fit-content;
}

.toc h3 {
  margin-bottom: 1rem;
  font-size: 1.2rem;
}

.toc ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.toc li {
  margin-bottom: 0.5rem;
}

.toc li a {
  text-decoration: none;
  color: #333;
  cursor: pointer;
}

.toc li.active a {
  font-weight: 700;
  color: #007bff;
}

.whitepaper-page ul {
  padding-left: 1.2rem;
  margin-top: 0.5rem;
}

.whitepaper-page ul li {
  margin-bottom: 0.5rem;
}

</style>
