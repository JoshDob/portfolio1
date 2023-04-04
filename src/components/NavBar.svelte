<!-- NavBar.svelte -->
<script>
  import Logo from "./Logo.svelte";
  import NavItem from "./NavItem.svelte";
</script>

<nav class="navbar">
  <Logo text="Your Site" />
  <ul class="nav-list">
    <NavItem label="Home" href="#home" />
    <NavItem label="About" href="#about" />
    <NavItem label="Skills" href="#skills" />
    <NavItem label="Projects" href="#projects" />
    <NavItem label="Contact" href="#contact" />
  </ul>
</nav>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: var(--spacing-medium);
    background-color: var(--bg-color);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .nav-list {
    display: flex;
    gap: var(--spacing-medium);
    list-style-type: none;
    padding: 0;
    margin: 0;
  }
</style>
