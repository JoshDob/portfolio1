<script>
  import Hero from "../components/Hero.svelte";
  import About from "./About.svelte";
  import Skills from "./Skills.svelte";
  import Projects from "./Projects.svelte";
</script>

<section class="home">
  <Hero />
</section>
<About />
<Projects />
<Skills />

<style>
  .home {
    position: relative;
    background-color: var(--bg-color);
    color: var(--text-color);
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  .container {
    z-index: 0;
  }

  h1 {
    font-size: 3rem;
    margin-bottom: var(--spacing-medium);
  }

  p {
    font-size: 1.5rem;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 2.5rem;
    }

    p {
      font-size: 1.2rem;
    }
  }
</style>
