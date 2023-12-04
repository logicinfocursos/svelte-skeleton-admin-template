<script>
  import setup from "../../configurations/setup.json";
  const __SETUP__ = setup.topmenu;
</script>

<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container">
    <a class="navbar-brand" href="/">svelte skeleton admin</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        {#each __SETUP__ as { href, title, status }}
          {#if status === 1}
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" {href}>{title}</a>
            </li>
          {/if}
        {/each}

        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle"
            href="/login"
            id="navbarDropdown"
            role="button"
            data-bs-toggle="dropdown"
            aria-expanded="false"
          >
            login
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="/">perfil</a></li>
            <li><hr class="dropdown-divider" /></li>
            <li><a class="dropdown-item" href="/">logout</a></li>
          </ul>
        </li>
      </ul>
      <form class="d-flex">
        <input
          class="form-control me-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-outline-success" type="submit">procurar</button>
      </form>
    </div>
  </div>
</nav>
