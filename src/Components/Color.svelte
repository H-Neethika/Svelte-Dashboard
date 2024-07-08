<!-- Color.svelte -->
<script>
  export let color;
  export let text;

  function getOuterColor(color) {
    // Define colors for the outer circle based on the main color
    switch (color) {
      case '#FFEBCC':
        return '#FFA500'; // Example alternate color for the outer circle
      case '#D9F2E6':
        return '#3CB371';
      case '#F0E5FF':
        return '#9370DB';
      case '#FFCCC9':
        return '#FF6347';
      case '#CBD5E0':
        return '#718096'; // Gray color
      case '#C8E5F6':
        return '#57C0FE';// Blue color
      default:
        return '#e5e7eb'; // Default outer color
    }
  }



  function getIconPath(color) {
    // Define SVG paths based on the main color
    switch (color) {
      case '#FFEBCC':
        return `
          <path fill="none" stroke="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
         	<path fill="white" d="M10 16v-1H3v4c0 1.11.89 2 2 2h14c1.11 0 2-.89 2-2v-4h-7v1zm10-9h-4V5l-2-2h-4L8 5v2H4c-1.1 0-2 .9-2 2v3c0 1.11.89 2 2 2h6v-2h4v2h6c1.1 0 2-.9 2-2V9c0-1.1-.9-2-2-2m-6 0h-4V5h4z" />
     `;
      case '#D9F2E6':
        return `
          <path fill="none" stroke="#3CB371" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
        	<path fill="white" d="M12 9c1.59 7.61-2 13-2 13h3c1.88-5.8 1-9.91.5-12m2.16-2.84c.17.21.34.43.47.66a7.1 7.1 0 0 1-.63 8.44a7.11 7.11 0 0 0-.55-6.49c-.08-.13-.17-.24-.25-.36a7.1 7.1 0 0 0-2.16-1.98a7.13 7.13 0 0 0-4.96 6.79c0 .74.11 1.45.31 2.11a7.07 7.07 0 0 1-1.33-4.14c0-2.35 1.14-4.43 2.89-5.73C8 6.35 6.46 6.67 5.12 7.5q-.93.615-1.62 1.41C4.05 7.58 5 6.39 6.3 5.57c1.5-.94 3.2-1.25 4.84-1.01C10.73 4 10.23 3.47 9.63 3c-.58-.42-1.21-.76-1.87-1c1.44.04 2.88.5 4.11 1.43c.63.47 1.13 1.04 1.53 1.64c.1 0 .19-.01.29-.01c3.2 0 5.91 2.11 6.81 5.02a7.07 7.07 0 0 0-4.84-2.92" />
        `;
      case '#F0E5FF':
        return `
          <path fill="none" stroke="#9370DB" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
         	<path fill="white" d="m17.73 12l3.98-3.96c.39-.39.39-1.04 0-1.41l-4.34-4.34c-.37-.39-1.02-.39-1.41 0L12 6.27L8 2.29a1 1 0 0 0-1.41 0L2.25 6.63c-.39.37-.39 1.02 0 1.41L6.23 12l-3.98 4c-.39.39-.39 1 0 1.41l4.34 4.34c.41.39 1.02.39 1.41 0l4-3.98l3.96 3.98c.2.2.45.29.71.29s.51-.1.71-.29l4.34-4.34c.39-.41.39-1.02 0-1.41zM12 9a1 1 0 0 1 1 1a1 1 0 0 1-1 1a1 1 0 0 1-1-1a1 1 0 0 1 1-1m-4.71 1.96L3.66 7.34l3.63-3.63l3.62 3.62zM10 13a1 1 0 0 1-1-1a1 1 0 0 1 1-1a1 1 0 0 1 1 1a1 1 0 0 1-1 1m2 2a1 1 0 0 1-1-1a1 1 0 0 1 1-1a1 1 0 0 1 1 1a1 1 0 0 1-1 1m2-4a1 1 0 0 1 1 1a1 1 0 0 1-1 1a1 1 0 0 1-1-1a1 1 0 0 1 1-1m2.66 9.34l-3.63-3.62l3.63-3.63l3.62 3.62z" />
        `;
      case '#FFCCC9':
        return `
          <path fill="none" stroke="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
          <path fill="white" d="M16 3a1 1 0 0 1 1 1v1h2a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V7a2 2 0 0 1 2-2h2V4a1 1 0 0 1 2 0v1h6V4a1 1 0 0 1 1-1M8 7H5v2h14V7h-3zm-3 4v8h14v-8zm2 2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H8a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H12a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H16a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2z" />
      `;
      case '#CBD5E0':
        return `
         <path fill="none" stroke="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
       		<path fill="white" d="M15.764 4a3 3 0 0 1 2.683 1.658l1.386 2.771q.366-.15.72-.324a1 1 0 0 1 .894 1.79a32 32 0 0 1-.725.312l.961 1.923A3 3 0 0 1 22 13.473V16a3 3 0 0 1-1 2.236V19.5a1.5 1.5 0 0 1-3 0V19H6v.5a1.5 1.5 0 0 1-3 0v-1.264c-.614-.55-1-1.348-1-2.236v-2.528a3 3 0 0 1 .317-1.341l.953-1.908q-.362-.152-.715-.327a1.01 1.01 0 0 1-.45-1.343a1 1 0 0 1 1.342-.448q.355.175.72.324l1.386-2.77A3 3 0 0 1 8.236 4zM7.5 13a1.5 1.5 0 1 0 0 3a1.5 1.5 0 0 0 0-3m9 0a1.5 1.5 0 1 0 0 3a1.5 1.5 0 0 0 0-3m-.736-7H8.236a1 1 0 0 0-.832.445l-.062.108l-1.27 2.538C7.62 9.555 9.706 10 12 10c2.142 0 4.101-.388 5.61-.817l.317-.092l-1.269-2.538a1 1 0 0 0-.77-.545L15.765 6Z" />
        `;
      case '#C8E5F6':
        return `
          <path fill="none" stroke="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
          <path fill="white" d="M16 3a1 1 0 0 1 1 1v1h2a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V7a2 2 0 0 1 2-2h2V4a1 1 0 0 1 2 0v1h6V4a1 1 0 0 1 1-1M8 7H5v2h14V7h-3zm-3 4v8h14v-8zm2 2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H8a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H12a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H16a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2z" />

        `;
      default:
        return `
          <path fill="none" stroke="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 8V3h14v5M7 21V10h10v11" />
          <path fill="#e5e7eb" d="M16 3a1 1 0 0 1 1 1v1h2a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V7a2 2 0 0 1 2-2h2V4a1 1 0 0 1 2 0v1h6V4a1 1 0 0 1 1-1M8 7H5v2h14V7h-3zm-3 4v8h14v-8zm2 2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H8a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H12a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2zm3-2a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2H16a1 1 0 0 1-1-1m1 2a1 1 0 1 0 0 2h.01a1 1 0 1 0 0-2z" />
        `;
    }
  }
</script>

<div class="color-box" style="background-color: {color};">
  <div class="content">
    <div class="outer" style="background-color: {getOuterColor(color)};">
      <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" class="icon" style="color: {getOuterColor(color)};">
        <!-- Dynamic icon path based on color -->
        <g>
          {@html getIconPath(color)}
        </g>
      </svg>
    </div>
    <p class="days">{text.split('\n')[0]}</p>
    <p class="description">{text.split('\n')[1]}</p>
    <p class="days-used">0 Days Used</p>
  </div>
</div>

<style>
  .outer {
    /* Styling for the outer circle */
    font-size: 18px;
    background-color: #e5e7eb; /* Default outer color */
    color: #374151;
    border-radius: 50%;
    padding: 2px;
    display: flex;
    width: 20px;
    height: 20px;
    align-items: center;
    justify-content: center;
  }

  .color-box {
    /* Styling for the color box */
    color: #333;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    border-radius: 8px;
    padding: 10px 15px;
    align-items: flex-start; 
    width: 110px;
    height: 120px;
   
  }

  .content {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start; 
    height: 100%; /* Ensure content fills entire height */
  }

  .days {
    font-size: 1.4rem;
    font-weight: 700;
    color: #33475b;
    margin: 0;
  }

  .description {
    font-size: 0.8rem;
    color: #425166;
    font-weight: 600;
    margin: 0;
  }

  .days-used {
    color: #4079ed;
    font-size: 0.7rem;
    font-weight: 500;
    margin: 0;
  }

  /* Dynamic icon color based on color prop */
  .icon path {
    fill: currentColor; /* Fill color dynamically */
    stroke: currentColor; /* Stroke color dynamically */
  }
</style>
