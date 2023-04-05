<script>
  import { writable } from "svelte/store";
  const menuOpen = writable(false);

  function toggleMenu() {
    $menuOpen = !$menuOpen;
  }
</script>

<div class="nav-bar">
  <div class="logo" on:click={toggleMenu}>
    <img src="/logo.svg" alt="Logo" />
    <div class="line" />
  </div>
  {#if $menuOpen}
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  {/if}
</div>

<style>
  .nav-bar {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10;
    padding: 1rem;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .logo {
    cursor: pointer;
  }

  .line {
    width: 50%;
    height: 2px;
    background-color: currentColor;
    margin-top: 0.2rem;
  }

  nav {
    margin-top: 1rem;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  a {
    color: inherit;
    text-decoration: none;
    font-size: 1.1rem;
  }

  a:hover {
    color: var(--accent-color);
  }
</style>
