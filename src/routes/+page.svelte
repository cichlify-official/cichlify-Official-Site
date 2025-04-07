<!-- File: src/routes/+page.svelte -->
<script>
    import Header from '../Components/Header.svelte';
    import Grid from '../Components/Grid.svelte';
    import Footer from '../Components/Footer.svelte';
  </script>
  
  <div class="container">
    <Header />
    <Grid />
    <Footer />
  </div>
  
  <style>
    .container {
      max-width: 1400px;
      margin: 0 auto;
      padding: 3rem 2rem;
      min-height: 100vh;
      background-color: var(--dark);
      color: var(--light-gray);
      font-family: var(--font-main);
      line-height: 1.6;
    }
  
    @media (max-width: 768px) {
      .container {
        padding: 2rem 1.5rem;
      }
    }
  </style>
  