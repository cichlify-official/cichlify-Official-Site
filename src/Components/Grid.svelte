<!-- File: src/components/Grid.svelte -->
<script>
    import { fly, } from 'svelte/transition';
    const items = [
      {
        title: 'Innovative Software Solutions',
        description: 'Discover our suite of products designed to streamline operations and boost productivity across your organization.',
        button: 'Explore Products',
        class: 'item-1'
      },
      {
        title: 'Tech Insights Blog',
        description: 'Stay ahead of the curve with our expert analysis on the latest technology trends and innovations.',
        button: 'Our Blog',
        class: 'item-2'
      },
      {
        title: 'Support Center',
        description: 'Get answers to your questions with our dedicated support team.',
        button: 'Get Help',
        class: 'item-3'
      },
      {
        title: 'Our Story',
        description: 'From visionary beginnings to industry leadership, learn about our journey and the team behind our success.',
        button: 'Our History',
        class: 'item-4'
      },
      {
        title: 'Ready for Digital Transformation?',
        description: 'Schedule a consultation with our experts to discuss how we can elevate your business with custom software solutions.',
        button: 'Contact Us Today',
        class: 'item-5'
      }
    ];
  </script>
  
  <section class="grid-container">
    {#each items as item, i}
      <div
        class="grid-item {item.class}"
        in:fly={{ y: 30, duration: 400, delay: i * 150 }}
      >
        <h2>{item.title}</h2>
        <p>{item.description}</p>
        <button class="btn">{item.button}</button>
      </div>
    {/each}
  </section>
  
  <style>
    .grid-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: repeat(3, 250px);
      gap: 1.5rem;
      margin-bottom: 3rem;
    }
  
    .grid-item {
      background-color: var(--dark-gray);
      border-radius: 16px;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
      border: 1px solid rgba(255, 255, 255, 0.05);
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
  
    .grid-item:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 24px var(--primary);
      border-color: var(--primary);
    }
  
    .grid-item h2 {
      font-size: 1.5rem;
      font-weight: 600;
    }
  
    .grid-item p {
      font-size: 1rem;
      opacity: 0.8;
      margin-bottom: 1.5rem;
    }
  
    .btn {
      width: 50%;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      color: #fff;
      border: none;
      border-radius: 40px;
      padding: 1rem 1.8rem;
      font-size: 0.9rem;
      font-weight: 600;
      cursor: url('src/assets/cichlify cursor.png'), auto;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }
  
    .btn::after {
      content: '→';
      transition: transform 0.3s ease;
    }
  
    .btn:hover::after {
      transform: translateX(3px);
    }
  

    .item-1 {
      grid-column: 1 / 3;
      background: linear-gradient(135deg,#282b28);
      transition: all 0.3s ease;
    }
    .item-1:hover {
      background-image: 
      linear-gradient(135deg, #282b28, rgba(8, 8, 8, 0.1)),
      url('/Images/innovation.jpg'); 
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
           
    }

  
    .item-2 {
      grid-column: 3 / 4;
      grid-row: 1 / 3;
      background: linear-gradient(135deg,#282b28);
    }

    .item-2:hover {
      background-image: 
      linear-gradient(135deg, #282b28, rgba(8, 8, 8, 0.1)),
      url('/Images/insight.jpg'); 
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
    }
  
    .item-3 {
      grid-column: 1 / 2;
      grid-row: 2 / 4;
      background: linear-gradient(135deg,#282b28);
    }

    .item-3:hover {
      background-image: 
      linear-gradient(135deg, #282b28, rgba(8, 8, 8, 0.1)),
      url('/Images/support.jpg'); 
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
    }
    .item-4 {
      grid-column: 2 / 3;
      grid-row: 2 / 3;
      background: linear-gradient(135deg,#282b28);
    }

    .item-4:hover {
      background-image: 
      linear-gradient(135deg, #282b28, rgba(8, 8, 8, 0.1)),
      url('/Images/story.jpg'); 
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
    }
  
    .item-5 {
      grid-column: 2 / 4;
      grid-row: 3 / 4;
      background: linear-gradient(135deg,#282b28);
    }

    .item-5:hover {
      background-image: 
      linear-gradient(135deg, #282b28, rgba(8, 8, 8, 0.1)),
      url('/Images/ready.jpg'); 
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
    }
  
    @media (max-width: 1024px) {
      .grid-container {
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(4, 220px);
      }
  
      .item-1 { grid-column: 1 / 3; }
      .item-2 { grid-column: 1 / 2; grid-row: 2 / 4; }
      .item-3 { grid-column: 2 / 3; grid-row: 2 / 3; }
      .item-4 { grid-column: 2 / 3; grid-row: 3 / 4; }
      .item-5 { grid-column: 1 / 3; grid-row: 4 / 5; }
    }
  
    @media (max-width: 768px) {
    
      .grid-item h2{
        font-size: 1.2rem;
      }

      .btn{
        width: 100%;
        padding: 0.5rem;
        font-size: 0.8rem;
      }

      .grid-item p{
        font-size: 0.9rem;
      }
      .grid-container {
        grid-template-columns: 1fr;
        grid-template-rows: auto;
      }
  
      .grid-item {
        padding: 1.2rem;
        grid-column: auto !important;
        grid-row: auto !important;
        height: 250px;
      }
    }
  </style>
  