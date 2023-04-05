<script>
  import Hero from "../components/Hero.svelte";
  import About from "./About.svelte";
  import Skills from "./Skills.svelte";
  import Projects from "./Projects.svelte";

  let scrollY = 0;
  let sections;

  function handleScroll(event) {
    scrollY = event.target.scrollTop;
  }

  function isVisible(section) {
    return scrollY > section.offsetTop - section.offsetHeight;
  }

  sections = [
    { component: About, offsetTop: 0, offsetHeight: 0 },
    { component: Projects, offsetTop: 0, offsetHeight: 0 },
    { component: Skills, offsetTop: 0, offsetHeight: 0 },
  ];
</script>

<section class="home">
  <div class="fixed-container" on:scroll={handleScroll}>
    <Hero />
    {#each sections as section}
      {#if isVisible(section)}
        <section>
          <svelte:component this={section.component} />
        </section>
      {/if}
    {/each}
  </div>
</section>

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

  .fixed-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    overflow-x: hidden;
    overflow-y: auto;
  }

  section {
    position: absolute;
    top: 0;
    left: 100%;
    width: 100%;
    transition: left 0.5s ease;
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
