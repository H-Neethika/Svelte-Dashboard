<script>
  import "@fortawesome/fontawesome-free/css/all.css";
  let clockedInTime = "--:--"; // Example clocked-in time
  let clockedOutTime = "--:--"; // Example clocked-out time
  let totalHours = "--:--"; // Example total hours
  let isClockedIn = true; // Example state
  import { LogOut, LogIn, History, Pointer } from "lucide-svelte";
</script>

<div class="clock-section">
  <h3 style="margin-top: 0%;">{isClockedIn ? "Clock In" : "Clock Out"}</h3>
  <div class="clockdiv">
    <div style="display: flex; justify-content: center;">
      <button class="clock-btn" on:click={() => (isClockedIn = !isClockedIn)}>
        <div
          style="display: flex; flex-direction: column; align-items: center; justify-content:space-between;"
        >
          {#if isClockedIn}
          <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M8 13V4.5a1.5 1.5 0 0 1 3 0V12m0-.5v-2a1.5 1.5 0 0 1 3 0V12m0-1.5a1.5 1.5 0 0 1 3 0V12"></path><path d="M17 11.5a1.5 1.5 0 0 1 3 0V16a6 6 0 0 1-6 6h-2h.208a6 6 0 0 1-5.012-2.7L7 19q-.468-.718-3.286-5.728a1.5 1.5 0 0 1 .536-2.022a1.87 1.87 0 0 1 2.28.28L8 13M5 3L4 2m0 5H3m11-4l1-1m0 4h1"></path></g></svg>
            <!-- Adjust size as needed -->
            <h5 style="margin-top: 5px;">Clock In</h5>
            <!-- Adjust margin as needed -->
          {:else}
          <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M8 13V4.5a1.5 1.5 0 0 1 3 0V12m0-.5v-2a1.5 1.5 0 0 1 3 0V12m0-1.5a1.5 1.5 0 0 1 3 0V12"></path><path d="M17 11.5a1.5 1.5 0 0 1 3 0V16a6 6 0 0 1-6 6h-2h.208a6 6 0 0 1-5.012-2.7L7 19q-.468-.718-3.286-5.728a1.5 1.5 0 0 1 .536-2.022a1.87 1.87 0 0 1 2.28.28L8 13M5 3L4 2m0 5H3m11-4l1-1m0 4h1"></path></g></svg>
            <!-- Adjust size as needed -->
            <h5 style="margin-top: 5px;">Clock Out</h5>
            <!-- Adjust margin as needed -->
          {/if}
        </div>
      </button>
    </div>
    <div class="time-info">
      <div class="time-item">
        <LogOut size={16} color="#737791" />
        <div>{clockedInTime}</div>
        <small class="time-label">Clocked In</small>
      </div>
      <div class="time-item">
        <LogIn size={16} color="#737791" />
        <div>{clockedOutTime}</div>
        <small class="time-label">Clocked Out</small>
      </div>
      <div class="time-item">
        <History size={16} color="#737791" />
        <div>{totalHours}</div>
        <small class="time-label">Total Hrs</small>
      </div>
    </div>
  </div>
</div>

<style>
  .clockdiv {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    gap: 26px;
  }
  .clock-section {
    margin: auto;
  }

  .clock-btn {
    cursor: pointer;
    background: none;
    border: 1px solid rgba(56, 114, 202, 0.5); /* Blue border */
    border-radius: 50%;
    width: 100px;
    height: 100px;

    flex-direction: column;
    align-items: center;
   
    box-shadow: 0 0 10px rgba(56, 114, 202, 0.5); /* Blue shadow */
    transition: all 0.3s;
    color: #2d2a28; /* Dark gray color */
  }

  .clock-btn:hover {
    box-shadow: 0 0 10px rgba(112, 201, 124, 0.7); /* Green shadow on hover */
    color: #1f2937; /* Darker gray on hover */
    border: 1px solid rgba(112, 201, 124, 0.7);
  }
  .time-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .time-item {
    text-align: center;
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  .time-icon {
    font-size: 24px;
    margin-bottom: 5px;
    color: #4b5563; /* Dark gray color */
  }

  .time-label {
    margin-bottom: 0;
    font-size: 12px;
    font-weight: 500;
    color: #737791;
  }

  h3 {
    /* padding: 0 0 10px 0;
    margin: 0; */
    color: #33475b;

    font-size: 14px;
    font-weight: 600;
  }

  h5{
    margin: 0;
  }
  @media (max-width: 480px) {
    .clock-section {
      padding: 10px;
    }

    .clock-btn {
      width: 80px;
      height: 80px;
    }

    .time-info {
      flex-direction: column;
    }
  }
</style>
