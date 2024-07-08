<script>
  // State to track the dropdown visibility
  let isOpen = false;

  // Function to toggle the dropdown
  function toggleDropdown() {
    isOpen = !isOpen;
  }

  // Close the dropdown when clicking outside of it
  function handleClickOutside(event) {
    if (!event.target.closest(".dropdown")) {
      isOpen = false;
    }
  }

  // Listen for clicks outside the dropdown to close it
  document.addEventListener("click", handleClickOutside);

  // Cleanup event listener on component destroy
  import { onDestroy } from "svelte";
  onDestroy(() => {
    document.removeEventListener("click", handleClickOutside);
  });
</script>

<div class="dropdown">
  <!-- Dropdown Button -->
  <button class="dropdown-button" on:click={toggleDropdown}>
    <span class="maindrop"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="20"
        height="20"
        viewBox="0 0 24 24"
        ><g fill="none" fill-rule="evenodd"
          ><path
            d="M24 0v24H0V0zM12.594 23.258l-.012.002l-.071.035l-.02.004l-.014-.004l-.071-.036q-.016-.004-.024.006l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.016-.018m.264-.113l-.014.002l-.184.093l-.01.01l-.003.011l.018.43l.005.012l.008.008l.201.092q.019.005.029-.008l.004-.014l-.034-.614q-.005-.018-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.003-.011l.018-.43l-.003-.012l-.01-.01z"
          ></path><path
            fill="currentColor"
            d="M11 13q.671 0 1.316.07a1 1 0 0 1-.211 1.989Q11.564 15 11 15c-2.023 0-3.843.59-5.136 1.379c-.647.394-1.135.822-1.45 1.222c-.324.41-.414.72-.414.899c0 .122.037.251.255.426c.249.2.682.407 1.344.582C6.917 19.858 8.811 20 11 20l.658-.005a1 1 0 0 1 .027 2L11 22c-2.229 0-4.335-.14-5.913-.558c-.785-.208-1.524-.506-2.084-.956C2.41 20.01 2 19.345 2 18.5c0-.787.358-1.523.844-2.139c.494-.625 1.177-1.2 1.978-1.69C6.425 13.695 8.605 13 11 13m7.5 0a2.5 2.5 0 0 1 2.495 2.336L21 15.5v.585c.538.19.935.678.993 1.266L22 17.5v3a1.5 1.5 0 0 1-1.356 1.493L20.5 22h-4a1.5 1.5 0 0 1-1.493-1.356L15 20.5v-3a1.5 1.5 0 0 1 .869-1.361l.131-.054V15.5a2.5 2.5 0 0 1 2.5-2.5m1.5 5h-3v2h3zm-1.5-3a.5.5 0 0 0-.5.5v.5h1v-.5a.5.5 0 0 0-.5-.5M11 2a5 5 0 1 1 0 10a5 5 0 0 1 0-10m0 2a3 3 0 1 0 0 6a3 3 0 0 0 0-6"
          ></path></g
        ></svg
      >
      Jitu Jaisi
    </span>
    <!-- <span class="opt">Jitu Jaisi</span> -->
    <span style=" font-size: 8px; cursor:pointer;color:#808080">▼</span>
  </button>

  <!-- Dropdown Menu -->
  {#if isOpen}
    <div class="dropdown-menu">
      <div class="dropdown-item">
        <span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            ><g fill="none" fill-rule="evenodd"
              ><path
                d="M24 0v24H0V0zM12.594 23.258l-.012.002l-.071.035l-.02.004l-.014-.004l-.071-.036q-.016-.004-.024.006l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427q-.004-.016-.016-.018m.264-.113l-.014.002l-.184.093l-.01.01l-.003.011l.018.43l.005.012l.008.008l.201.092q.019.005.029-.008l.004-.014l-.034-.614q-.005-.018-.02-.022m-.715.002a.02.02 0 0 0-.027.006l-.006.014l-.034.614q.001.018.017.024l.015-.002l.201-.093l.01-.008l.003-.011l.018-.43l-.003-.012l-.01-.01z"
              ></path><path
                fill="currentColor"
                d="M11 13q.671 0 1.316.07a1 1 0 0 1-.211 1.989Q11.564 15 11 15c-2.023 0-3.843.59-5.136 1.379c-.647.394-1.135.822-1.45 1.222c-.324.41-.414.72-.414.899c0 .122.037.251.255.426c.249.2.682.407 1.344.582C6.917 19.858 8.811 20 11 20l.658-.005a1 1 0 0 1 .027 2L11 22c-2.229 0-4.335-.14-5.913-.558c-.785-.208-1.524-.506-2.084-.956C2.41 20.01 2 19.345 2 18.5c0-.787.358-1.523.844-2.139c.494-.625 1.177-1.2 1.978-1.69C6.425 13.695 8.605 13 11 13m7.5 0a2.5 2.5 0 0 1 2.495 2.336L21 15.5v.585c.538.19.935.678.993 1.266L22 17.5v3a1.5 1.5 0 0 1-1.356 1.493L20.5 22h-4a1.5 1.5 0 0 1-1.493-1.356L15 20.5v-3a1.5 1.5 0 0 1 .869-1.361l.131-.054V15.5a2.5 2.5 0 0 1 2.5-2.5m1.5 5h-3v2h3zm-1.5-3a.5.5 0 0 0-.5.5v.5h1v-.5a.5.5 0 0 0-.5-.5M11 2a5 5 0 1 1 0 10a5 5 0 0 1 0-10m0 2a3 3 0 1 0 0 6a3 3 0 0 0 0-6"
              ></path></g
            ></svg
          ></span
        >

        <span class="opt">Jitu Jaisi</span>
      </div>
      <div class="dropdown-item">
        <span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            ><path
              fill="currentColor"
              d="M12 23C6.443 21.765 2 16.522 2 11V5l10-4l10 4v6c0 5.524-4.443 10.765-10 12M4 6v5a10.58 10.58 0 0 0 8 10a10.58 10.58 0 0 0 8-10V6l-8-3Z"
            ></path><circle cx="12" cy="8.5" r="2.5" fill="currentColor"
            ></circle><path
              fill="currentColor"
              d="M7 15a5.78 5.78 0 0 0 5 3a5.78 5.78 0 0 0 5-3c-.025-1.896-3.342-3-5-3c-1.667 0-4.975 1.104-5 3"
            ></path></svg
          ></span
        >
        <span class="opt">Admin Controls</span>
      </div>
    </div>
  {/if}
</div>

<style>
  .maindrop {
    display: flex;
    gap: 7px;
    align-items: center;
  }
  /* Style for the dropdown */
  .dropdown {
    position: relative;
    display: inline-block;
  }

  /* Style for the button */
  .dropdown-button {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 9px 10px !important;
    border-radius: 8px !important;
    border: 2px solid #566a7f11 !important;
    font-size: 14px !important;
    background-color: #fff !important;
    color: #33475b !important;
    width: 200px;
  }

  /* Style for the dropdown menu */
  .dropdown-menu {
    position: absolute;
    top: 100%;
    left: 0;
    background-color: #fff;
    width: 200px;
    z-index: 1;
    margin-top: 5px;
    color: #33475b;
    font-size: 12px;
    border: 2px solid #566a7f11;
    padding: 8px;
    border-radius: 8px;
  }

  /* Style for the dropdown items */
  .dropdown-item {
    padding: 5px;
    cursor: pointer;
    font-size: inherit;
    display: flex;
    gap: 10px;
    align-items: center;
  }

  .dropdown-item:last-child {
    border-bottom: none;
  }

  .dropdown-item:hover {
    background-color: #f1f1f1;
  }

  .opt {
    color: #33475b;
  }
</style>
