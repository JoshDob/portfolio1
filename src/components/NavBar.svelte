<script>
  import { onMount } from "svelte";
  import NavItem from "./NavItem.svelte";
  import Logo from "./Logo.svelte";

  let scrolled = false;

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 50;
    };

    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  });

  const scrollTo = (id) => {
    const element = document.getElementById(id);
    element.scrollIntoView({ behavior: "smooth" });
  };
</script>

<nav class="navbar" class:scrolled>
  <Logo />
  <div class="nav-items">
    <NavItem>
      <a href="#home" on:click={() => scrollTo("home")}>Home</a>
    </NavItem>
    <NavItem>
      <a href="#about" on:click={() => scrollTo("about")}>About</a>
    </NavItem>
    <NavItem>
      <a href="#skills" on:click={() => scrollTo("skills")}>Skills</a>
    </NavItem>
    <NavItem>
      <a href="#projects" on:click={() => scrollTo("projects")}>Projects</a>
    </NavItem>
    <NavItem>
      <a href="#contact" on:click={() => scrollTo("contact")}>Contact</a>
    </NavItem>
  </div>
</nav>

<style>
  nav {
    /* Add a semi-transparent background */
    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(5px);

    /* Add smooth transitions */
    transition: all 0.3s ease;
  }

  nav:hover {
    /* Make the background more opaque when hovering */
    background: rgba(0, 0, 0, 0.8);
  }
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.66rem 1.3rem;
    position: fixed;
    top: 0;
    left: 0;
    height: 33%;
    width: 9%;
    z-index: 1000;
    background-color: rgba(0, 0, 0, 0.4);
  }

  .nav-items {
    display: flex;
    gap: 1.5rem;
  }

  .navbar.scrolled {
    background-color: rgba(0, 0, 0, 0.8);
    transition: background-color 0.3s ease-in-out;
  }
</style>
