<!-- File: src/components/Header.svelte -->
<section class="header">
    <h1>Cichlify</h1>
    <p>Transform your digital presence with our cutting-edge software solutions tailored to your business needs</p>
  </section>
  
  <style>
    .header {
      margin-bottom: 3rem;
      text-align: center;
    }
  
    .header h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
      font-weight: 800;
      letter-spacing: -0.05em;
      background: linear-gradient(90deg, white, white);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
  
    .header p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 0 auto;
      opacity: 0.9;
    }
  
    @media (max-width: 768px) {
      .header h1 {
        font-size: 2.2rem;
      }
    }
  </style>
  