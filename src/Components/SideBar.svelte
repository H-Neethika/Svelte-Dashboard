<script>
  // Import icons from lucide-svelte
  import {
    House,
    CalendarCheck,
    CircleUserRound,
    UsersRound,
    CalendarClock,
    UserRoundSearch,
    FileText,
    UserRoundCheck,
    ListTodo,
    RefreshCcwDot,
    GraduationCap,
    Banknote,
    HandCoins,
    CopyCheck,
    Settings,
    ArrowLeft,
    ArrowRight,
  } from "lucide-svelte";

  export let activePage = "";
  let sidebarCollapsed = false;

  const sidebarItems = [
    { label: "Home", icon: House },
    { label: "Approvals", icon: CalendarCheck },
    { label: "Profile Information", icon: CircleUserRound },
    { label: "People", icon: UsersRound },
    { label: "Leave Management", icon: CalendarClock },
    { label: "Hiring", icon: UserRoundSearch },
    { label: "Files", icon: FileText },
    { label: "Attendance", icon: UserRoundCheck },
    { label: "Project Tracking", icon: ListTodo },
    { label: "Rostering", icon: RefreshCcwDot },
    { label: "Training", icon: GraduationCap },
    { label: "Payroll", icon: Banknote },
    { label: "Claims", icon: HandCoins },
    { label: "Surveys", icon: CopyCheck },
    { label: "Settings", icon: Settings },
  ];

  function toggleSidebar() {
    sidebarCollapsed = !sidebarCollapsed;
  }
</script>

<div class="sidebar" class:collapsed={sidebarCollapsed}>
  <ul>
    {#each sidebarItems as item}
      <li class:active={activePage === item.label}>
        <svelte:component
          this={item.icon}
          class="sidebar-icon"
          aria-label={item.label}
        />
        {!sidebarCollapsed ? item.label : ""}
      </li>
    {/each}
  </ul>
  <div class="toggle-button" on:click={toggleSidebar}>
    {#if sidebarCollapsed}
      <div class="current">
        <ArrowRight class="arrow-icon" size={20} />
      </div>
    {:else}
      <div class="current">
        <ArrowLeft class="arrow-icon" size={20} />
        <span>Shrink Panel</span>
      </div>
    {/if}
  </div>
</div>

<style>
  /* Sidebar styles */
  .arrow-icon {
    height: 16px;
    width: 16px;
    margin-right: 5px;
  }
  .sidebar {
    width: 200px;
    padding: 10px 0;
    height: 100vh;
    position: fixed;
    left: 0;
    font-size: 10px;
    font-weight: normal;
    transition: width 0.5s;
    background-color: #ffffff;
    margin-top: 40px;
  }
  .sidebar.collapsed {
    width: 55px;
    align-items: center;
  }
  .sidebar ul {
    list-style-type: none;
    padding-left: 5px;
    flex-direction: column;
  }
  .sidebar ul li {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 5px;
    cursor: pointer;
    padding: 7px;
    border-radius: 5px;
    transition: background-color 0.3s;
    margin: 5px;
    color: #33475b;
    height: 15px;
  }
  .sidebar ul li:hover {
    background-color: #dfeffc;
    color: #0e5e92;
  }
  .sidebar-icon {
    margin-right: 5px;
    height: auto;
    width: 16px;
    justify-content: flex-start;
  }
  /* .sidebar:not(.collapsed) .sidebar-icon {
    width: 16px;
    height: auto;
  } */
  .sidebar ul li.active {
    background-color: #eeeeee;
    color: #0e5e92;
  }
  .collapsed .sidebar ul li {
    justify-content: center;
  }
  .toggle-button {
    margin-bottom: 5px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 5px;
    cursor: pointer;
    padding: 5px;
    border-radius: 5px;
    transition: background-color 0.3s;
    margin-left: 15px;
    color: #33475b;
    height: 15px;
  }
  .toggle-button:hover {
    background-color: #dfeffc;
    color: #0e5e92;
  }
  .current {
    display: flex;
    align-items: center;
    gap: 5px;
    padding-left: 10px;
  }
  /* Media query for medium screens */
  @media (max-width: 992px) {
    .sidebar {
      width: 180px;
    }
  }
  /* Media query for extra small screens */
  @media (max-width: 480px) {
    .sidebar {
      width: 120px;
    }
  }
</style>
