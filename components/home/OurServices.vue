<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="What is Skaina?"
        heading="Introducing Skaina"
        description="Skaina is a next-generation blockchain designed to preserve what truly matters: documents, patents, proofs, records, and digital assets that must never be lost, altered, or destroyed.
Built for permanence. Engineered for truth. Powered by a decentralized network that protects your legacy — forever."
        style="max-width: 64rem"
      />
      <app-section-descriptor
        title="Our mission"
        heading="Skaina Vision"
        style="max-width: 60rem"
      />
            <app-section-descriptor
            description="Vision: A world where no essential document, proof or record can ever disappear.
Mission: To provide a decentralized, censorship-resistant ledger capable of storing and validating information for centuries.

Skaina is not just a blockchain — it is a digital monument to truth."
style="text-align: left;" />
<div class="spc"></div>

      <app-section-descriptor
            description="Skaina is more than a blockchain — it is a digital vault for humanity’s most valuable information.
A platform where truth is permanent, documents live forever, and legacy becomes unbreakable."
style="text-align: left;" />
<div class="spc"></div>
      <div class="overview-features">
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="icon-container">
            <v-image class="serv-image" 
            path="images/sphere_261.png" 
            alt="Skaina Security" />
          </div>
          <div class="overview-feature">
            <v-heading :level="2" class="overview-feature-title">
              Security
            </v-heading>
            <v-heading :level="2" class="overview-feature-title">
            </v-heading>
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >     
              <ul>
      <li> Data Protection: Uses advanced encryption to secure data at rest and in transit.</li>
      <li>Access Control: Role-based authentication ensures only authorized users can access sensitive data.</li>
      <li>Threat Resistance: Defends against tampering, spoofing, and unauthorized access.</li>

    </ul>  
             



              </v-text>
                           

  


            </div>
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
                Privacy
             
              </v-heading>

            </div>
            
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >                 <ul>
      <li> User-Controlled Data: Users manage what data they share and with whom.</li>
      <li>Confidential Transactions: Sensitive actions are performed without exposing underlying data.</li>
      <li>Minimal Exposure: The system reduces unnecessary data collection and sharing.</li>

    </ul>  

                    </v-text>
            </div>
          </div>
          <div class="icon-container">
            <v-image class="serv-image"
              path="images/sphere_262.png"
              alt="Skaina Privacy"
            />
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="icon-container">
            <v-image class="serv-image1"
              path="images/sphere_263.png"
              alt="Skaina Scalability"
            />
          </div>
          <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
                Immutability
              </v-heading>
            </div>
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
                             <ul>
      <li> Tamper-Proof Records: Once data is recorded, it cannot be modified or deleted without detection.</li>
      <li>Audit Trail: Every change or transaction generates a cryptographic record, enabling full traceability.</li>
      <li>Data Integrity: Guarantees that historical data remains intact and verifiable, critical for compliance and trust.</li>

    </ul>     
              </v-text>
              
            </div>
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <!-- <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
            Scalability           
             </v-heading>
            </div>
            
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
               >                 <ul>
      <li> Data Protection: Skaina employs state-of-the-art encryption (both symmetric and asymmetric) to secure data at rest and in transit.</li>
      <li>Access Control: Role-based access and authentication mechanisms ensure that only authorized users can access sensitive information.</li>
      <li>Threat Resistance: Built-in protections against common cyber threats like tampering, spoofing, and unauthorized access.</li>

    </ul> 
              </v-text>
            </div>
          </div> -->
          <!-- <div class="icon-container">
            <v-image class="serv-image"
              path="images/eco5.png"
              alt="Skaina Eco"
            />
          </div> -->
        </v-stack>
        
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'Features',
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

section {
  padding-bottom: 6rem;

  @media (--viewport-small) {
    padding-bottom: 3rem;
  }
}

.overview-description {
  max-width: 52ch;
  font-size: 1.25rem;

  @media (--viewport-small) {
    font-size: 1rem;
  }
}

.overview-feature {
  max-width: 40rem;
  text-align: left;
}

.overview-features > * {
  margin-top: 6rem;

  @media (--viewport-small) {
    margin-top: 3rem;
  }
}

.overview-feature-title {
  margin: 0;
  font-size: 2.25rem;
  line-height: 1.5;

  @media (--viewport-small) {
    font-size: 1.25rem;
  }
}

.overview-feature-description {
  margin-top: 1.25rem;
}

.feature-description-text {
  color: #000;
  font-size: 1.375rem;

  @media (--viewport-small) {
    font-size: 0.875rem;
  }
}
.serv-image{
  max-width: 100%;
}
.serv-image1{
  max-width: 100%;
}
.icon-container {
  position: relative;
  overflow: visible;
}

/* .icon-container::before {
  content: '';
  position: absolute;
  top: -40%;
  left: -40%;
  right: -40%;
  bottom: -40%;
  z-index: -1;
  background: radial-gradient(
    45% 40% at 50% 50%,
    rgba(112, 239, 207, 0.3) 0%,
    rgba(0, 0, 0, 0) 100%
  );
  filter: blur(5px);
} */

.icon-container:nth-child(2)::before {
  background: radial-gradient(
    45% 40% at 50% 50%,
    rgba(112, 239, 207, 0.3) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}

.icon-container > * {
  @media (--viewport-medium) {
    width: 10rem;
    margin-top: 1rem;
  }

  @media (--viewport-small) {
    width: 6rem;
    margin-top: 0.5rem;
  }
}
</style>
