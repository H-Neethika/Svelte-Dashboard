<script>
  import { writable } from "svelte/store";

  // Create a writable store to manage the selected option
  const selected = writable("All");

  // Define the options for the radio buttons
  const options = ["All", "Office", "Remote"];

  // Function to handle click events
  function handleClick(option) {
    selected.set(option);
  }
</script>

<style>
  .segmented-button {
    display: flex;
    position: relative;
    border: 1px solid #ccc;
    border-radius: 5px;
    overflow: hidden;
    width: fit-content;
    cursor: pointer;
  }

  .option {
    flex: 1;
    padding: 10px 20px;
    text-align: center;
    user-select: none;
    color: #33475b;
    justify-content: space-around;
    font-size: 12px;
    font-weight: 600;
  }

  .selected {
    background-color: rgba(0, 0, 0, 0.03);
    color: #33475b;
    transition: all 0.5s ease;
    width: 33.3%;
    
  }
  /* .hover-effect {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    width: calc(100% / 3);
    background-color: rgba(0, 0, 0, 0.03);
    transition: left 0.5s ease;
    pointer-events: none;
  } */

  /* Adjust width based on the number of options */
  .segmented-button[data-options="3"] .hover-effect {
    width: calc(100% / 3);
  }

  .segmented-button[data-options="2"] .hover-effect {
    width: calc(100% / 2);
  }

  .segmented-button[data-options="1"] .hover-effect {
    width: 100%;
  }
</style>

<div
  class="segmented-button"
  data-options={options.length}
  aria-label="Segmented control for view options"
>
  {#each options as option}
    <div
      class="option"
      on:click={() => handleClick(option)}
      class:selected={$selected === option}
      aria-selected={$selected === option}
      role="button"
    >
      {option}
    </div>
  {/each}
  <div
    class="hover-effect"
    style="left: calc(100% / {options.length} * {options.indexOf($selected)}); "
  ></div>
</div>
