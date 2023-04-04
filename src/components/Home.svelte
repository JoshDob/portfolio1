<script>
  import AnimatedWave from "./AnimatedWave.svelte";
</script>

<section class="home">
  <AnimatedWave />
  <div class="container">
    <h1>Joshua Dobrowner</h1>
    <p>Full-Stack Web Developer</p>
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

  .container {
    z-index: 1;
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
