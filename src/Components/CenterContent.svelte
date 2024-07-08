<script>
  import Carouseldiv from "./Carouseldiv.svelte";
  import SegmentedButton from "./SegmentedButton.svelte";
  import Clockin from "./Clockinout.svelte";
  import { Grip, House, Bell } from "lucide-svelte";
  import Calendar from "./Calendar.svelte";
  import MembersSection from "./MembersSection.svelte";
  import Companylinks from "./Companylinks.svelte";

  let isHovered = false;

  function handleHover() {
    isHovered = !isHovered;
  }

  // Import icons from lucide-svelte
  import {
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
    Search,
  } from "lucide-svelte";
  import Mytrainings from "./Mytrainings.svelte";
  import Dropdown from "./Dropdown.svelte";
  import Trainingicon from "./Trainingicon.svelte";

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

<main>
  <div class="root">
    <div class="main-content">
      <div style="justify-content:space-between">
        <!-- Top bar content like Clock In, User Profile goes here -->
        <div class="navbar">
          <div class="leftcontent">
            <Grip
              size={20}
              strokeWidth={3}
              style="color: {isHovered ? '#33475b' : '#33475B'}"
              on:mouseover={handleHover} 
              on:mouseout={handleHover}
            />
            <div class="title">
              <img src="/logo.webp" alt="Logo" class="logo" />
            </div>
            <div class="current">
              <House size={20} />
              <span>Home</span>
            </div>
          </div>
          <div class="rightcontent">
            <img
              src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAMAAABF0y+mAAAA5FBMVEVHcEwD/NKEat8M8daRYuBWh+1fgfBspKcD+tZre+Ii2duZW+Fdg+1Nm+SZW9o/vd1ileJYguVXg+oR99BRqOEC/tgXF0wYLWNag+oKE0kaEkoS5d5GnetUiepTi+4Y3OFMk+s0vORRj+wM7ttjfetdg+8WIlmbWeeRYuUJ9NhYh+6Bc+FHnOBVouOHaegPCkUi2NtJsN8xx9kX7No7reY6jLg1ort2cuslzOVzguBoj+Ebyb4fbogmTX5ne99DpOgmtLdbgd9RjOA7s9IqOHMCADoblp0LUGhPh8AGJEpnaL5KaKUph+3HAAAAFXRSTlMAu9PAxFhXBP7EwK2KFVDAwEVYfMAEKgTPAAABaklEQVQokaXSa0/CMBSAYYmoQy5e29FOYBcYDBwFxgTcJuDG/f//H0/bcfWLiW/S7MOT06zJubr6T8VC7lBWli+l9lSu1xt13mg06nZbTVFeYll2qSU5KJrPv3idThe41Wq2xOizNNWWJdvUs3usVOYqxpRSfnYdUY7jTQUyvwHVJElsisl2wjtHsnbd6Rq+0Sc0eUzRNHWBw+Gwv2M4cnkH1AEp8Q0oxDTqQ+6rxKqpv73DpB/HsW9jFhoG6MMZUltVbYKpGo8H0DmKp2C8mvV4g3uBVYkUR2FEsD2wNE2r1XoS2+2qQPJRG6iULS3H8jRPE3jbOKK2ZHQTKI5led71L+ytKAsdxYFSbFTlUwC9GSEkQAq0x7bJkQFaXsjYyuOaOUW24OgEm8ViiZCCTnDq+77B0Qlms0BBSGJR4tAYj2saKEp7ETtUaFd0jgZH+E3EL0VKun4FU08n+b2KmMsUj6t7d9Eftv0HWaJP/2KU0yQAAAAASUVORK5CYII="
              alt="profile"
            />
            <button class="bellbtn">
              <span class="notification">13</span>
              <Bell />
            </button>
            <div>
              <Dropdown />
            </div>
            <div class="search">
              <div class="luicide">
                <Search />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div
        class="content"
        style="margin-left: {sidebarCollapsed ? '60px' : '200px'}"
      >
        <div class="widgets">
          <div class="widget">
            <div class="row1">
              <div class="subcol">
                <div class="subcol1">
                  <div
                    style="display:flex;justify-content: space-between; align-items:center"
                  >
                    <div>
                      <h3>Leave Information</h3>
                      <small class="subdes">
                        Revolutionizing Employee Leave Management
                      </small>
                    </div>
                    <div>
                      <button class="btn">Request Leave</button>
                    </div>
                  </div>

                  <Carouseldiv />
                </div>
                <div class="subcol2">
                  <Clockin />
                </div>
              </div>
            </div>
            <div class="row">
              <div style="display:flex;justify-content: space-between; ">
                <div>
                  <h3>My Current Tasks</h3>
                  <small class="subdes">Track All Of Your Tasks Easily</small>
                </div>
                <div>
                  <button class="btn">View All</button>
                </div>
              </div>
              <div class="blank"></div>
            </div>
            <div class="row">
              <MembersSection />
            </div>

            <div class="row">
              <div style="display:flex;justify-content: space-between; ">
                <div>
                  <h3>Today's Attendance</h3>
                  <small class="subdes">
                    Check Who's Online or Offline in Your Circle on Tuesday ,
                    2nd July 2024
                  </small>
                </div>
                <div>
                  <!-- <button class="btn">All | Office | Remote</button> -->
                  <SegmentedButton />
                </div>
              </div>
              <div class="blank"></div>
            </div>
          </div>

          <div class="widget2">
            <div class="row">
              <Calendar />
              <hr style="color: #e5e7eb" />

              <div>
                <h3>Events</h3>

                <div class="blank"></div>
              </div>
              <hr style="color: #f0f2f4" />
              <div style="display:flex;justify-content: center; gap:20px; ">
                <div>
                  <button class="btn">All Celebrations</button>
                </div>
                <div>
                  <button class="btn">Full Calendar</button>
                </div>
              </div>
            </div>
            <div class="row">
              <Companylinks />
            </div>
            <div class="row">
              <Mytrainings />
            </div>
          </div>
        </div>
      </div>
      <div
        style="margin-left: {sidebarCollapsed
          ? '60px'
          : '200px'};display:flex;justify-content:space-between;"
      >
        <div class="leftcontent">
          Privacy Policy · 2024 RomeoHR All rights reserved.
        </div>
        <div class="botrightcontent">
          <img
            src="https://www.romeohr.com/images/logo/logo.webp"
            alt="Logo"
            class="bottomlogo"
          />
        </div>
      </div>
    </div>

    <div class="sidebar" class:collapsed={sidebarCollapsed}>
      <ul>
        {#each sidebarItems as item}
          <li class:active={activePage === item.label}>
            <svelte:component
              this={item.icon}
              class="sidebar-icon"
              aria-label={item.label}
              size="14px"
            />
            {!sidebarCollapsed ? item.label : ""}
          </li>
        {/each}
      </ul>
      <div class="toggle-button" on:click={toggleSidebar}>
        {#if sidebarCollapsed}
          <div class="current1">
            <ArrowRight class="arrow-icon" size={20} />
          </div>
        {:else}
          <div class="current1">
            <ArrowLeft class="arrow-icon" size={20} />
            <span>Shrink Panel</span>
          </div>
        {/if}
      </div>
    </div>
  </div>
</main>

<style>
  /* Base styles */
  .bottomlogo {
    height: 20px;
    margin: 10px 0;
  }
  .search {
    position: relative;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    /* Light blue background */
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer; /* Optional: Add pointer cursor on hover */
    transition: background-color 0.3s ease;
    color: #33475b;
  }

  .search:hover {
    background-color: #f2f6f8;
  }

  .search .luicide {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 24px; /* Adjust icon size */
    height: 24px;
    /* Icon color */
  }
  .bellbtn {
    color: #566a7f;
    background-color: #fff;
    border: none;
    border-radius: 50%;
    padding: 8px;
    width: 40px;
    height: 40px;
  }
  .notification {
    position: absolute;
    top: 0;
    right: 0;
    padding: 0.2rem 0.3rem;
    background-color: var(--primary);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    font-size: 0.582rem;
  }
  .navbar {
    height: 65px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    width: 100%;
    z-index: 500;
    background-color: #fff;
    top: 0;
  }

  body,
  html {
    margin: 0;
    padding: 0;
    font-family: Inter, sans-serif;
    font-size: x-small;
    background-color: #ffffff;
    color: #33475b;
  }

  /* Root container */
  .root {
    display: flex;
  }

  .rightcontent {
    display: flex;
    align-items: center;
    gap: 2px;
    flex-direction: row-reverse;
    padding-right: 40px;
  }
  .botrightcontent {
    display: flex;
    align-items: center;
    gap: 2px;
    flex-direction: row-reverse;
    padding-right: 10px;
  }
  .current {
    display: flex;
    align-items: center;
    gap: 5px;
    padding-left: 10px;
    border-left: 5px solid #f2f6f8;
    color: #505050;
    font-weight: 600;
    font-size: 20px;
  }

  h3 {
    color: #33475b;
    margin: 0;
    font-size: 14px;
    font-weight: 600;
  }

  /* Main content styles */
  .main-content {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }



  .leftcontent {
    margin-left: 20px;
    display: flex;
    align-items: center;
    font-size: 0.8rem;
    font-weight: 500;
    color: #737791;
  }
  .title {
    padding: 0%;
  }

  .content {
    padding: 20px;
    flex-grow: 1;
    margin: 60px 30px 10px 0;
    background-color: #f2f6f8;
    border-radius: 16px;
    margin-top: 70px;
    transition: margin-left 0.5s; /* Add transition for smooth animation */
    overflow: hidden;
  }

  .content-collapsed {
    padding: 20px;
    flex-grow: 1;
    margin: 60px 20px 80px 50px;
    background-color: #f2f6f8;
    border-radius: 10px;
    margin-top: 60px;
    transition: margin-left 0.5s; /* Add transition for smooth animation */
    overflow: hidden;
  }

  .widgets {
    display: grid;
    grid-template-columns: 65% 35%;
    gap: 15px;
  }

  .widget {
    background-color: #f2f6f8;
    padding: 0;
    border-radius: 10px;
  }
  .widget2 {
    background-color: #f2f6f8;
    margin-right: 15px;
    border-radius: 10px;
    height: fit-content;
  }

  .blank {
    padding: 20px;
    flex-grow: 1;
    min-height: 100px;
    background-color: #f2f6f8;
    border-radius: 10px;
    margin: 15px 0 0 0;
  }
  .row {
    padding: 20px;
    background-color: #ffffff;
    gap: 10px;
    margin-bottom: 15px;
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid #e5e7eb;
  }

  .row1 {
    background-color: #ffffff;
    gap: 10px;
    margin-bottom: 15px;
    height: auto;
    overflow: hidden;
  }

  .subcol {
    display: grid;
    grid-template-columns: 65% 35%;
    margin: 0;
    background-color: #f2f6f8;
    height: 100%;
  }

  .subcol1 {
    padding: 20px;
    border-radius: 10px;
    margin-right: 15px;
    background-color: #ffffff;
    overflow: hidden;
    border: 1px solid #e5e7eb;
  }

  .subcol2 {
    padding: 20px;
    background-color: #ffffff;
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid #e5e7eb;
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

  .subdes {
    font-size: 12px;
    font-weight: 400;
    color: #737791;
  }

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
    cursor: pointer;
    padding: 5px;
    border-radius: 5px;
    transition: background-color 0.3s;
    margin-left: 10px;
    color: #33475b;
    height: 15px;
    
  }
  .toggle-button:hover {
    background-color: #dfeffc;
    color: #0e5e92;
   
  }
  .current1 {
    display: flex;
    align-items: center;
    gap: 5px;
  }
  /* Media query for medium screens */
  @media (max-width: 992px) {
    .sidebar {
      width: 180px;
    }
    .widgets {
      grid-template-columns: 1fr; /* Change to single column */
    }
    .content {
      margin-left: 180px; /* Adjust margin for medium screens */
    }
  }

  @media (max-width: 768px) {
    .sidebar {
      width: 200px;
    }
    .widgets {
      grid-template-columns: 1fr;
    }

    .content {
      margin-left: 200px; /* Adjust for smaller screens */
    }
  }

  /* Media query for extra small screens */
  @media (max-width: 480px) {
    .sidebar {
      width: 120px;
    }

    .content {
      margin-left: 120px; /* Further adjust margin for extra small screens */
    }
  }
</style>
