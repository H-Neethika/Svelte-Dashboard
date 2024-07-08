<script>
  import { Link2 } from "lucide-svelte";
</script>

<div style="display:flex;justify-content: space-between; align-items:center">
  <div>
    <h3>Company Links</h3>
  </div>
  <div>
    <button class="btn">Details</button>
  </div>
</div>
<div class="links">
  <div class="comlink">
    <p>RomeoHR Links</p>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      RomeoHR Home
    </a>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      Package Pricing
    </a>
  </div>

  <div class="comlink">
    <p>Other Links</p>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      Why RomeoHR ?
    </a>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      RomeoHR Customer Support
    </a>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      RomeoHR Story
    </a>
  </div>

  <div class="comlink">
    <p>Help Requests</p>
    <a class="linkinfo">
      <div class="linkbtn">
        <Link2 color="#0f6ba3" />
      </div>
      RomeoHR F&Q
    </a>
  </div>
</div>

<style>
  p {
    font-size: 0.8rem;
    font-weight: 500;
    color: #737791;
    padding: 0;
  }

  .linkinfo {
    padding: 5px 0;
    text-decoration: none;
    font-size: 0.75rem;
    font-weight: 600;
    color: #33475b;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: 0.3s ease-in-out;
  }
  .btn {
    background: none;
    border: 1px solid #e5e7eb;
    background-color: transparent;
    cursor: pointer;
    font-family: inherit;
    font-size: 10px;
    align-items: center;
    border-radius: 8px;
    padding: 8px 16px;
    font-weight: 600;
    color: #33475b;
    transition: all 0.4s;
  }

  .btn:hover {
    border-color: black; /* Change border color on hover */
  }

  .comlink {
    display: flex;
    flex-direction: column;
  }
  .linkbtn {
    border-radius: 5px;
    background-color: #dfeffc;
    align-items: center;
    justify-content: center;
    padding: 5px;
  }

  h3 {
    color: #33475b;
    margin: 0;
    font-size: 14px;
    font-weight: 600;
  }
</style>
