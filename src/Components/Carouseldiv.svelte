<script>
  import Carousel from 'svelte-carousel';
  import Color from './Color.svelte';

  let colors = [
    { color: '#FFEBCC', text: '7 DAYS\nBereavement' },
    { color: '#D9F2E6', text: '14 DAYS\nVacation' },
    { color: '#F0E5FF', text: '10 DAYS\nSick' },
    { color: '#FFCCC9', text: '10 DAYS\nCovid-19 Absence' },
    { color: '#CBD5E0', text: '5 DAYS\nFMLA' },
    { color: '#C8E5F6', text: '12 DAYS\nComp/ln Liey Time' }
  ];
</script>

<main>
  
  <Carousel
    autoplay
    autoplayDuration={3000}
    particlesToShow={3}
    particlesToScroll={1}
    dots={false}
    arrows={false}
  >
    {#each colors as { color, text } (color)}
      <div class="carousel-item">
        <Color {color} {text} />
      </div>
    {/each}
  </Carousel>
</main>

<style>
  .carousel-item {
    margin-left: -20px; /* Space between each item */
    cursor: pointer;
    min-width: fit-content;
  }

  main {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 20px;
  }
 
</style>
