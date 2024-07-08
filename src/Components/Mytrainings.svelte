<script>
  import { Link2 } from "lucide-svelte";
  import Trainingicon from "./Trainingicon.svelte";
</script>

<div style="display:flex;justify-content: space-between; ">
  <div>
    <h3>My Trainings</h3>
    <small class="subdes">Review All Your Training Schedules</small>
  </div>
  <div>
    <button class="btn">View All</button>
  </div>
</div>
<div class="training">
  <h6 style="display: flex; justify-items:center;align-items:center">
    <Trainingicon />
    <span class="task">Compliance Training</span>
  </h6>
  <div class="allitem">
    <div class="list">
      <a class="listitem"> Data privacy and security training </a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem"> Financial compliance training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem"> Policies and procedures training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
  </div>
</div>

<div class="training">
  <h6 style="display: flex; justify-items:center;align-items:center">
    <Trainingicon />
    <span class="task">Professional Development Training</span>
  </h6>
  <div class="allitem">
    <div class="list">
      <a class="listitem"> Leadership and management training </a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Communication and interpersonal skills training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Company culture and values training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem"> Customer service and relationship-building training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
  </div>
</div>

<div class="training">
  <h6 style="display: flex; justify-items:center;align-items:center">
    <Trainingicon />
    <span class="task">Technical Training</span>
  </h6>
  <div class="allitem">
    <div class="list">
      <a class="listitem"> Code of conduct training </a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Technical and job-specific training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem"> Job-specific training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Software training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Technical skills training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Equipment training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Product knowledge training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
    <div class="list">
      <a class="listitem">Industry-specific training</a>
      <div class="date">
        <p class="dot">.</p>
        <small class="datepart"> Due July 3rd, 2024 </small>
      </div>
    </div>
  </div>
</div>

<style>
  .datepart {
    font-size: 10px;
    color: #737791;
  }
  .dot {
    color: red;
    font-size: 30px;
    font-weight: bolder;
    border-radius: 50%;
    position: absolute;
    display: flex;
    align-items: center;
    justify-items: center;
    transform: translate(-14px, -8px);
  }
  .date {
    display: flex;
    white-space: nowrap;
    border: 1px solid #737791;
    border-radius: 20px;
    align-items: center;
    padding: 4px 10px 4px 20px;
    font-weight: 500;
    position: relative;
  }
  .listitem {
    font-size: 0.8rem;
    font-weight: 500;
    color: #737791;
    text-decoration: none;
    margin-left: 32px;
    width: 60%;
  }
  .list {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .allitem {
    display: flex;
    flex-direction: column;
    border-left: 3px solid #e5e7eb;
    gap: 16px;
    margin-left: 19px;
  }
  .training {
    display: flex;
    flex-direction: column;
  }
  .task {
    padding: 5px 20px;
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
  p {
    font-size: 0.8rem;
    font-weight: 500;
    color: #737791;
    padding: 0;
  }
  .subdes {
    font-size: 12px;
    font-weight: 400;
    color: #737791;
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
