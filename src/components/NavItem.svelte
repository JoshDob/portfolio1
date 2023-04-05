<script>
  export let onClick;
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="nav-item" on:click={onClick}>
  <slot />
</div>

<style>
  .nav-item {
    font-size: 1.1rem;
    font-weight: 600;
    cursor: pointer;
  }

  .nav-item:hover {
    color: var(--accent-color);
  }
</style>
