<script>
  export let backgroundColor = "var(--bg-color)";
  export let gradientStart = "var(--gradient-start)";
  export let gradientEnd = "var(--gradient-end)";
</script>

<div class="background" style="background-color: {backgroundColor};">
  <div
    class="gradient"
    style="background: linear-gradient(135deg, {gradientStart} 0%, {gradientEnd} 100%);"
  />
</div>

<style>
  .background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -2;
  }

  .gradient {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.7;
    z-index: -1;
  }
</style>
