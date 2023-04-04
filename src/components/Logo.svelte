<script>
  export let text = "My Site";
</script>

<div class="logo-container">
  <a href="#" class="logo">{text}</a>
</div>

<style>
  :root {
    --logo-font-size: 1.5rem;
  }

  .logo-container {
    display: flex;
    align-items: center;
  }

  .logo {
    font-size: var(--logo-font-size);
    font-weight: bold;
    text-transform: uppercase;
    color: var(--text-color);
    text-decoration: none;
  }
</style>
