<script>
  import setup from "../../configurations/setup.json";
  const __SETUP__ = setup.sidebarMenu;
</script>

<div
  class="d-flex flex-column vh-100 flex-shrink-0 p-3 text-white bg-dark"
  style="width: 250px;"
>
<img
src="https://github.com/mdo.png"
alt=""
width="32"
height="32"
class="rounded-circle me-2"
/> 
  <a
    href="/"
    class="d-flex align-items-center mb-3 mb-md-0 me-md-auto text-white text-decoration-none"
  >
    <svg class="bi me-2" width="40" height="32"> </svg>
    <span class="fs-4">BBBootstrap</span>
  </a>
  <hr />
  <ul class="nav nav-pills flex-column mb-auto">

    {#each __SETUP__ as { href, title, status }}
    {#if status === 1}
    <li class="nav-item">
        <a {href}class="nav-link" aria-current="page">
          <i class="bi bi-house-fill"></i><span class="ms-2">{title}</span>
        </a>
      </li>
    {/if}
  {/each}

  </ul>
  <hr />
  <div class="dropdown">
    <a
      href="#"
      class="d-flex align-items-center text-white text-decoration-none dropdown-toggle"
      id="dropdownUser1"
      data-bs-toggle="dropdown"
      aria-expanded="false"
    >
     <strong> John W </strong>
    </a>
    <ul
      class="dropdown-menu dropdown-menu-dark text-small shadow"
      aria-labelledby="dropdownUser1"
    >
      <li><a class="dropdown-item" href="#">New project</a></li>
      <li><a class="dropdown-item" href="#">Settings</a></li>
      <li><a class="dropdown-item" href="#">Profile</a></li>
      <li><hr class="dropdown-divider" /></li>
      <li><a class="dropdown-item" href="#">Sign out</a></li>
    </ul>
  </div>
</div>
