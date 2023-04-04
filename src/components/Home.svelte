<script>
  import Background from "./Background.svelte";
</script>

<main>
  <Background>
    <div class="home-content container">
      <h1>Joshua Dobrowner</h1>
      <p>Full-stack web developer</p>
    </div></Background
  >
</main>

<style>
  :root {
    --home-title-font-size: 4rem;
    --home-subtitle-font-size: 2rem;
  }

  main {
    position: relative;
  }

  .home-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    z-index: 1;
  }

  .home-content h1 {
    font-family: "Montserrat", sans-serif;
    font-size: var(--home-title-font-size);
    margin-bottom: var(--spacing-medium);
    color: #fff;
    text-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }

  .home-content p {
    font-family: "Open Sans", sans-serif;
    font-size: var(--home-subtitle-font-size);
    margin-bottom: var(--spacing-large);
    color: #fff;
    text-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }

  @media (max-width: 768px) {
    :root {
      --home-title-font-size: 3rem;
      --home-subtitle-font-size: 1.8rem;
    }
  }
</style>
