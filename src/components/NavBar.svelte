<script>
  import { onMount } from "svelte";
  import Logo from "./Logo.svelte";
  import NavItem from "./NavItem.svelte";

  let scrolled = false;

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.pageYOffset > 50;
    };

    window.addEventListener("scroll", handleScroll);

    return () => {
      window.removeEventListener("scroll", handleScroll);
    };
  });
</script>

<header class:scrolled>
  <nav class="navbar">
    <Logo text="Joshua Dobrowner" />
    <div class="nav-items">
      <NavItem label="Home" href="#home" />
      <NavItem label="About" href="#about" />
      <NavItem label="Skills" href="#skills" />
      <NavItem label="Projects" href="#projects" />
      <NavItem label="Contact" href="#contact" />
    </div>
  </nav>
</header>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: var(--spacing-small) 0;
    background-color: transparent;
    transition: background-color 0.3s ease-in-out;
    z-index: 1000;
  }

  .scrolled {
    background-color: rgba(255, 255, 255, 0.9);
  }

  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 var(--spacing-medium);
  }

  .nav-items {
    display: flex;
    align-items: center;
    gap: var(--spacing-medium);
  }
</style>
