<!-- Footer.svelte -->
<footer>
  <div class="container">
    <p>&copy; {new Date().getFullYear()} Your Name. All rights reserved.</p>
  </div>
</footer>

<style>
  footer {
    background-color: var(--primary-color);
    color: #fff;
    padding: var(--spacing-medium);
  }

  .container {
    display: flex;
    justify-content: center;
  }

  footer p {
    font-size: 1.2rem;
    margin: 0;
  }
</style>
