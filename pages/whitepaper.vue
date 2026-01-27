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
          content: `Skaina is a next-generation blockchain designed to permanently preserve information that must never be lost, altered, or destroyed. Unlike conventional blockchains focused purely on financial transactions, Skaina is optimized for immutable data anchoring, decentralized timestamping, and verifiable proof-of-truth. It serves as a digital monument to human knowledge, capable of storing intellectual property, legal documents, certifications, medical records, digital identity, and long-term archives.`
        },
        {
          title: "2. Vision & Mission",
          content: `
            <p><strong>Vision:</strong> A world where no essential document can ever disappear.</p>
            <p><strong>Mission:</strong> To provide a decentralized, censorship-resistant ledger capable of storing and validating information
               for centuries.</p>
            <p><strong>Skaina</strong> is not just a blockchain — it is a permanent vault of truth.</p>         
          `
        },
        {
          title: "3. Core Principles",
          content: `<ul class="bullet-list">
                      <li󠁯>•󠁏<strong> Permanence:</strong> Once stored, data cannot be removed or altered.</li>
                      <li>󠁯•󠁏<strong> Integrity:</strong> Every block and transaction is cryptographically verifiable.</li>
                      <li>󠁯•󠁏<strong> Neutrality:</strong> No centralized authority can censor, modify, or intercept data.</li>
                      <li>󠁯󠁯•󠁏<strong> Longevity:</strong> Designed for decades-long sustainability of the blockchain.</li>
                      <li>󠁯•󠁏<strong> Utility:</strong> Supports both secure data anchoring and fast, decentralized payments.</li>         
                    </ul>`
        },
        {
          title: "4. Architecture Overview",
          content: `
            <p>Skaina employs a layered architecture to balance speed, security, and storage efficiency:</p>
            </br>
            <ul class="bullet-list">
                <li>•󠁏<strong> Layer 1:</strong> Core blockchain with sidechain-based scaling support</li>
                <li>•󠁏<strong> Consensus Engine:</strong> Tendermint Core, combining PoS and dBFT</li>
                <li>•󠁏<strong> PoS:</strong> BFT based consensus core with delegated participation</li>
                <li>•󠁏<strong> Instant finality:</strong> Handles validation, settlement, and security</li>
            </ul>
          `
        },
        {
          title: "5. Consensus & Blockchain Parameters",
          content: `<ul class="bullet-list">
                        <li>•󠁏<strong> Block Time:</strong> 2 seconds</li>
                        <li>•󠁏<strong> Block Size:</strong> Up to 20 MB</li>
                        <li>•󠁏<strong> Validators:</strong> Up to 51</li>
                        <li>•󠁏<strong> Minimum Stake per Validator:</strong> 5,000,000 SKA</li>
                        <li>•󠁏<strong> Validator Rotation:</strong> Yes, no slashing penalties</li>
                    </ul>
          `
        },
        {
          title: "6. Tokenomics",
          content: `
            <p><strong>Native Token:</strong> SKA</p>
            <p><strong>Supply & Distribution:</strong><p>
            <ul class="bullet-list">
              <li>•󠁏<strong>  Total Supply:</strong> 1,000,000,000 SKA (fixed)</li>
              <li>•󠁏<strong>  Premine:</strong> 25% allocated for initial development, partnerships, and early incentives</li>
              <li>•󠁏<strong>  Emission:</strong> 75% distributed via block rewards over 20 years</li>
              <li>•󠁏<strong>  Block Reward:</strong> 2.375 SKA per block</li>
            </ul>
            <p>Detailed allocation and vesting schedules will be transparently disclosed prior to mainnet launch.</p>
          `
        },
        {
        title: "7. Token Utility",
        content: `
          <p>
            <strong>SKA</strong> is the native utility token of the Skaina blockchain and is
            required for interaction with the protocol.
          </p>

          <ul>
            <li>•󠁏
              <strong>Transaction Fees:</strong>
              SKA is used to pay for transactions and on-chain operations.
            </li>

            <li>•󠁏
              <strong>Data Anchoring:</strong>
              Anchoring documents, hashes, and proofs requires SKA.
            </li>

            <li>•
              <strong>Network Security:</strong>
              Validators and delegators use SKA to secure the network and participate
              in consensus.
            </li>

            <li>•󠁏
              <strong>Governance:</strong>
              SKA grants the right to participate in protocol governance,
              either directly or through delegation.
            </li>
          </ul>

          <p>
            Additional utility extensions may be introduced over time.
          </p>
        `
      },
        {
          title: "8. Governance Model",
          content: `<p>
      Skaina governance is <strong>decentralized and community-driven</strong>, designed to balance network security,
      long-term stability, and broad stakeholder participation.
    </p>

                <ul class="bullet-list">
                  <li>•󠁏
                    <strong>Validators</strong> are responsible for block production, transaction validation,
                    and maintaining network consensus.
                  </li>
                  <li>•󠁏
                    <strong>Delegators</strong> may delegate their SKA tokens to trusted validators,
                    participating indirectly in network security and governance without running validator infrastructure.
                  </li>
                  <li>•󠁏
                    <strong>Token holders</strong> can participate in on-chain governance by voting on protocol upgrades,
                    economic parameters, and ecosystem initiatives, either directly or via delegated voting power.
                  </li>
                  <li>
            `
        },
        {
          title: "9. Token Economics",
          content: `
            <p>
              The Skaina network is powered by <strong>SKA</strong>, the native utility token
              used to operate, secure, and govern the protocol.
            </p>

            <ul>
              <li>•󠁏
                <strong>Network Usage:</strong>
                SKA is used to pay transaction fees and data anchoring costs on the Skaina blockchain.
              </li>

              <li>•󠁏
                <strong>Validators & Delegators:</strong>
                Validators earn SKA for securing the network, while delegators may support validators
                and participate in reward distribution.
              </li>

              <li>•󠁏
                <strong>Governance:</strong>
                SKA enables participation in on-chain governance, either directly or via delegation.
              </li>
            </ul>

            <p>
              Detailed economic parameters will be defined in Whitepaper 2.0.
            </p>
          `
        },
        // {
        //   title: "10. Roadmap",
        //   content: `<li>Phase 1 – Foundation: blockchain architecture, cryptographic model, whitepaper release.</li>
        //             <li>Phase 2 – Core Network: testnet, block explorer, wallet.</li>
        //             <li>Phase 3 – Mainnet Launch: validator onboarding, token distribution, exchange listing.</li>
        //             <li>Phase 4 – Ecosystem Expansion: L2 data anchoring protocol, developer SDK, institutional integrations.</li>`
        // },
        {
          title: "10. Conclusion",
          content: `Skaina is more than a blockchain — it is a <strong>digital vault for humanity’s most valuable information</strong>.<br />
            A platform where truth is permanent, documents live forever, and human legacy becomes unbreakable.<br /><br />
            <strong>Tagline:</strong> "Your legacy, our way. Forever."`
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

<style>
.whitepaper-container {
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  gap: 2rem;
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

/* WHITEPAPER CONTENT */
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

/* BULLET LISTS — GLOBAL SAFE */
.whitepaper-page .bullet-list {
  list-style: disc !important;
  padding-left: 1.5rem !important;
  margin: 0.75rem 0 !important;
}

.whitepaper-page .bullet-list li {
  display: list-item !important;
  margin-bottom: 0.5rem !important;
}
</style>
