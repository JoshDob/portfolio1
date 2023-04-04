<script>
  export let text;
  export let href;
  export let active;
</script>

<a
  {href}
  class="nav-item {active ? 'nav-item-active' : ''}"
  aria-current={active ? "page" : ""}>{text}</a
>

<style>
  .nav-item {
    font-size: 1.2rem;
    color: var(--text-color);
    text-decoration: none;
    padding: var(--spacing-small);
    margin: 0 var(--spacing-small);
    border-bottom: 2px solid transparent;
    transition: border-color 0.3s ease;
  }

  .nav-item:hover,
  .nav-item-active {
    border-color: var(--accent-color);
  }
</style>
