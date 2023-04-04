<!-- Background.svelte -->
<script>
  import AnimatedWave from "./AnimatedWave.svelte";
</script>

<AnimatedWave />

<div class="background">
  <div class="background-color" />
</div>

<style>
  :root {
    --gradient-start: #3e3e3e;
    --gradient-end: #292929;
    --background-opacity: 0.8;
  }

  .background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  .background-color {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    mix-blend-mode: screen;
    background-image: linear-gradient(
      to bottom,
      var(--gradient-start) 0%,
      var(--gradient-end) 100%
    );
    opacity: var(--background-opacity);
  }
</style>
