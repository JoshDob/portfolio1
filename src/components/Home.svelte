<script>
  import { onMount, onDestroy } from "svelte";
  import Hero from "../components/Hero.svelte";
  import About from "./About.svelte";
  import Skills from "./Skills.svelte";
  import Projects from "./Projects.svelte";

  let home;

  onMount(() => {
    home.addEventListener("scroll", handleScroll);
  });

  onDestroy(() => {
    home.removeEventListener("scroll", handleScroll);
  });

  function handleScroll() {
    const scrollY = home.scrollTop;
    const windowHeight = home.clientHeight;

    sections.forEach((section, index) => {
      const sectionTop = section.offsetTop;
      const sectionHeight = section.offsetHeight;
      const sectionBottom = sectionTop + sectionHeight;
      const sectionInView =
        scrollY + windowHeight * 0.75 > sectionTop && scrollY < sectionBottom;

      if (sectionInView) {
        const translateY =
          ((scrollY + windowHeight * 0.75 - sectionTop) / windowHeight) * 100;
        section.style.transform = `translateY(${100 - translateY}%)`;
      } else {
        section.style.transform = "translateY(100%)";
      }
    });
  }
</script>

<div class="hero-wrapper">
  <Hero />
</div>
<div class="home" bind:this={home}>
  <div class="sections-wrapper">
    <About />
    <Projects />
    <Skills />
  </div>
</div>

<style>
  .hero-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    z-index: -1;
    overflow: hidden;
  }

  .home {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow-y: scroll;
    scroll-behavior: smooth;
  }

  .sections-wrapper {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    height: 100%;
    transition: transform 0.5s ease;
    background-color: rgba(255, 255, 255, 0.85);
    backdrop-filter: blur(5px);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
  }

  .section {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    height: 100%;
    transition: transform 0.5s ease;
    background-color: rgba(255, 255, 255, 0.85);
    backdrop-filter: blur(5px);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
  }
</style>
