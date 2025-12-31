<template>
  <section>
    <!-- <div class="illustration-container">
      <v-image
        path="images/publications-illustration.svg"
        class="roadmap-illustration"
      />
    </div> -->
    <v-container>
      <v-stack direction="column">
        <app-section-descriptor title="Roadmap" heading="Skaina History & Roadmap" />
        <v-stack gap="1rem" class="laptop-remove">
          <v-dropdown
            v-model="selectedYear"
            :options="years"
            class="roadmap-dropdown"
          />
        </v-stack>
        <v-stack>
          <v-stack
            direction="column"
            style="margin: 1.5rem 6rem 0 0"
            class="tablet-remove mobile-remove"
          >
            <div v-for="year in years" :key="year">
              <v-chip
                class="clickable-chip"
                :class="{
                  'selected-year': selectedYear === year,
                }"
                @click="() => (selectedYear = year)"
              >
                <v-text :weight="600">{{ year }}</v-text>
              </v-chip>
            </div>
          </v-stack>
          <ul>
            <li
              v-for="item in roadmap[selectedYear]"
              :key="selectedYear + item.quarter"
            >
              <v-heading
                :level="4"
                :weight="600"
                font="serif"
                class="milestone-heading"
              >
                {{ item.quarter }} {{ selectedYear }}
              </v-heading>
              <div v-for="milestone in item.milestones" :key="milestone">
                <v-text
                  color="secondary"
                  :weight="400"
                  size="1.125rem"
                  class="milestone-description"
                >
                  {{ milestone }}
                </v-text>
              </div>
            </li>
          </ul>
        </v-stack>
      </v-stack>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'RoadmapList',
  data() {
    const selectedYear = new Date().getFullYear().toString()

    return {
      selectedYear,
      roadmap: {
        2026: [
        {
            quarter: 'Quarter 1',
            milestones: [
              'Skaina project development starts ✔️',
              ],
          },
          {
            quarter: 'Quarter 2',
            milestones: [
              'Skaina network testing - Closed Testnet ✔️',
            ],
          },
          {
            quarter: 'Quarter 3',
            milestones: [
              'Network stretching and bug fixes ✔️',
              ],
          },
          {
            quarter: 'Quarter 4',
            milestones: [
            'Skaina network testing - Public Testnet ✔️',
            ],
          },
        ],
        // 2027: [
        // {
        //     quarter: 'Quarter 1',
        //     milestones: [
        //       'Skaina Mainnet launch ✔️',
        //       'Whitepaper 1.0 release ✔️',
        //       'The roadmap for 2022 revealed ✔️',
        //       'Skaina community build - Airdrop ✔️',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 2',
        //     milestones: [
        //       'Skaina 2.0 web wallet development ✔️',
        //       'The new Skaina website development ✔️',
        //       'Whitepaper for Skaina 2.0 release ✔️',
        //       'NeatDocs documentation release ✔️',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 3',
        //     milestones: [
        //       'New website 2.0 look redesign ✔️',
        //       'AMA sesion with HedgePay project ✔️',
        //       'Staking website gets a new look ✔️',
        //       'Skaina 2.0 explorer redesign ✔️',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 4',
        //     milestones: [
        //       'Finexbox CEX listing of $SKA ✔️',
        //       'Discord and telegram bots release ✔️',
        //       'AMA sesion with AnyDAO project ✔️',
        //       'December Quest Competition ✔️',
        //       ],
        //   },
        // ],
        // 2028: [
        // {
        //     quarter: 'Quarter 1',
        //     milestones: [
        //       '2023 Roadmap presentation ✔️',
        //       'Skaina Blog development & launch ✔️',
        //       'Bitcointalk bounty campaign start ✔️',
        //       'Governance development & implementation ✔️',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 2',
        //     milestones: [
        //       '$SKA token contracts development ✔️',
        //       'Crosschain bridge contracts development ✔️',              
        //       '$SKA listing on DEX exchange ✔️',
        //       'Logo redesign for new $SKA network ✔️',
        //       'Whitepaper for Skaina 3.0 development ✔️',
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 3',
        //     milestones: [
        //       'Skaina network 3.0 development start ✔️',
        //       'The new website redesign and build ✔️',            
        //       'Contracts deployment on Polygon ✔️',
        //       'Uniswap v3 DEX $SKA token listing ✔️',
        //       'Undergoing native $SKA coin swap ✔️'
        //       ],
        //   },
        //   {
        //     quarter: 'Quarter 4',
        //     milestones: [
        //       'Complete native $SKA coin swap ✔️',
        //       'Skaina network 3.0 Testnet launch ✔️',
        //       'Skaina network 3.0 Mainnet launch ✔️',
        //       'New explorer for Skaina 3.0 development ✔️',
        //       'All-in-one wallet platform development ✔️',
        //       ],
        //   },
        // ],
        // 2029: [
        // // {
        // //     quarter: 'Quarter 1',
        // //     milestones: [
        // //       'ETH <-> SKA bridge development 💫' ,              
        // //       'NioDEX development and launch 💫' ,
        // //       'Listing Skaina on CoinMarketCap 💫',
        // //       'Listing Skaina on CoinGecko 💫',
                   
        // //       ],
        // //   },
        //   //  {
        //   //    quarter: 'Quarter 2',
        //   //    milestones: [
        //   //     'Asknio project development start 💫',
        //   //     'Validator development and launch 💫' ,
        //   //     'NFT integration (core update) 💫' ,
        //   //     'NFTs marketplace launch 💫' ,  
        //   //      ],
        //   //  },
        //   // {
        //   //   quarter: 'Quarter 3',
        //   //   milestones: [
        //   //     'Skaina Milestone 1',
        //   //     'Skaina Milestone 2',
        //   //     'Skaina Milestone 3',
              
        //   // },
        //   // {
        //   //   quarter: 'Quarter 4',
        //   //   milestones: [
        //   //     'Skaina Milestone 1',
        //   //     'Skaina Milestone 2',
        //   //     'Skaina Milestone 3',
        //   //     ],
        //   // },
        // ],
      },
    }
  },
  computed: {
    years() {
      return Object.keys(this.roadmap)
    },
  },
}
</script>

<style >
@import url('../lib/media-query-helper.css');

.roadmap-illustration {
  width: 100%;
  z-index: -1;
  margin-bottom: -12.5%;
}

.roadmap-dropdown {
  width: 50%;
  max-width: 12rem;
}

ul {
  padding: 0;
}

ul li {
  list-style: none;
}

.milestone-heading {
  margin: 1.5rem 0 0.5rem 0;
  font-size: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1.25rem;
  }
}

.milestone-description {
  font-size: 1.375rem;
  line-height: 2rem;

  @media (--viewport-medium) {
    font-size: 1rem;
    line-height: 1.5rem;
  }
}

.clickable-chip {
  background: radial-gradient(
    134.5% 939.99% at -23.59% -12.9%,
    #262626 0%,
    rgba(26, 26, 26, 0.86293) 31.41%,
    rgba(32, 32, 32, 0.49) 100%
  );
  box-shadow: 4px 5px 4px rgba(0, 0, 0, 0.25);
  padding: 1.5rem 5rem;
  margin: 1rem 2rem 0.5rem 0;
  cursor: pointer;
}

.clickable-chip > * {
  font-size: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1.25rem;
  }
}

.quarter {
  margin: 0.5rem 2rem 0.5rem 0;
  text-align: center;
  cursor: pointer;
}

.quarter > * {
  font-size: 1.25rem;
  line-height: 2.5rem;
}

.selected-year {
  border: 1px solid #FFF;
  border-radius: 10px;
}

.selected-year > * {
  color:#FFF;
  font-weight: 600;
}

.illustration-container {
  position: relative;
  z-index: -1;
}

.illustration-container::before {
  content: '';
  position: absolute;
  inset: -50% 0% -100% -50%;
  z-index: -1;
  background: radial-gradient(
    50% 50% at 50% 50%,
    rgba(248, 81, 142, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}
</style>
