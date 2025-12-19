<template>
  <main>
    <v-heading>Privacy Policy</v-heading>

    <div class="terms-title">INTRODUCTION</div>
    <div class="terms-text">
      This Privacy Policy describes how Skaina and/or SKA (“we,” “us,” or “our”) collects, uses, stores, and protects your information
      when you access or use the www.skaina.com website and its subdomains, including but not limited to blog.skaina.com,
      wallet.skaina.com, and scan.skaina.com (collectively, the “Website”).
    </div>

    <div class="terms-title">INFORMATION WE COLLECT</div>
    <div class="terms-text">
      Skaina does not knowingly collect personal identification information such as names, addresses, or government-issued IDs
      unless explicitly provided by you.

      <br /><br />
    
      We may automatically collect limited non-personal information, including:
      <ul>
        <li>Browser type and version</li>
        <li>Device type and operating system</li>
        <li>IP address (anonymized where possible)</li>
        <li>Usage statistics and interaction data</li>
      </ul>
    </div>

    <div class="terms-title">BLOCKCHAIN DATA</div>
    <div class="terms-text">
      Blockchain transactions are public by nature. Any data written to the blockchain, including wallet addresses and transaction
      metadata, is publicly accessible and cannot be altered or deleted. Skaina does not control or store blockchain data.
    </div>

    <div class="terms-title">USE OF INFORMATION</div>
    <div class="terms-text">
      Information collected is used solely to:
      <ul>
        <li>Maintain and improve the Website and services</li>
        <li>Monitor performance and security</li>
        <li>Prevent fraud, abuse, or malicious activity</li>
      </ul>
      We do not sell, rent, or trade your personal data to third parties.
    </div>


    </div>
  </main>
</template>

<style>
.terms-title {
  font-size: 1.375rem;
  line-height: 2rem;
  margin: 2.4rem 1rem;
  color: #000;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}

.terms-text {
  font-size: 1rem;
  line-height: 2rem;
  margin: 1rem;
  color: #000;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}
</style>
