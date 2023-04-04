<script>
  export let text;
</script>

<h1 class="logo">{text}</h1>

<style>
  .logo {
    font-size: 1.8rem;
    color: var(--text-color);
    text-decoration: none;
    margin: 0;
  }

  @media (max-width: 768px) {
    .logo {
      font-size: 1.5rem;
    }
  }
</style>
