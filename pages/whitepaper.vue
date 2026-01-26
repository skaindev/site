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
          title: "7. Use Cases",
          content: `
            <p>
              Skaina is designed as a <strong>general-purpose blockchain for permanent data preservation</strong>,
              enabling a wide range of use cases that require immutability, verifiable timestamps,
              and long-term integrity.
            </p>

            <ul>
              <li>
                <strong>Intellectual Property & Research</strong><br />
                Patents, inventions, source code, scientific research, and authorship proofs
                can be timestamped and anchored on Skaina to establish immutable proof of existence.
              </li>

              <li>
                <strong>Legal & Regulatory Documents</strong><br />
                Contracts, agreements, certificates, land titles, and compliance records
                can be permanently recorded to ensure authenticity, traceability, and auditability.
              </li>

              <li>
                <strong>Identity & Medical Records</strong><br />
                Secure identity proofs, credentials, and medical histories can be anchored
                while preserving user privacy through off-chain storage and cryptographic proofs.
              </li>

              <li>
                <strong>Corporate & Institutional Records</strong><br />
                Internal logs, corporate resolutions, governance records, and public disclosures
                can be stored to increase transparency and reduce reliance on centralized archives.
              </li>

              <li>
                <strong>Public Archives & Digital Heritage</strong><br />
                Cultural records, historical documents, academic archives, and digital artifacts
                can be preserved as part of a permanent, decentralized public ledger.
              </li>

              <li>
                <strong>Digital Payments & Network Utility</strong><br />
                SKA enables fast, decentralized value transfer and serves as the utility token
                for transaction fees, data anchoring, validation, and governance participation.
              </li>
            </ul>

            <p>
              These use cases position Skaina as a <strong>foundational layer for long-term data integrity</strong>,
              rather than a short-term transactional blockchain.
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
          title: "9. Security & Longevity",
          content: `<ul class="bullet-list">
                       <li>•󠁏 Advanced cryptographic protections</li>
                       <li>•󠁏 Multi-node consensus for fork resistance</li>
                       <li>•󠁏 Fraud proofs for long-term document integrity</li>
                       <li>•󠁏 Mechanisms for decades-long archival will be detailed in future updates</li>
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
