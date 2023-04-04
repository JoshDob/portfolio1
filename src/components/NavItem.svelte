<script>
  export let label;
  export let href;
</script>

<a {href}>
  <slot>{label}</slot>
</a>

<style>
  a {
    color: var(--text-color);
    text-decoration: none;
    padding: var(--spacing-small) var(--spacing-medium);
    transition: all 0.3s ease-in-out;
    position: relative;
    display: inline-block;
  }

  a:hover,
  a:focus {
    background-color: var(--bg-color);
    color: var(--accent-color);
  }

  a:focus::after {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 2px;
    background-color: var(--accent-color);
  }
</style>
