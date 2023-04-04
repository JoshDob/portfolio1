<script>
  export let skillName;
  export let skillLevel;
  export let skillIcon;
</script>

<div class="skill-card">
  <i class={skillIcon} />
  <h3>{skillName}</h3>
  <p class="level">{skillLevel}</p>
</div>

<style>
  .skill-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 200px;
    height: 200px;
    margin: var(--spacing-medium);
    border-radius: 10px;
    background-color: var(--bg-color);
    color: var(--text-color);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease-in-out;
  }

  .skill-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.25);
  }

  .skill-card i {
    font-size: 4rem;
    margin-bottom: var(--spacing-small);
    color: var(--primary-color);
  }

  .skill-card h3 {
    font-size: 1.5rem;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: var(--spacing-small);
  }

  .skill-card .level {
    margin-top: var(--spacing-xsmall);
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 600;
    color: var(--primary-color);
  }

  @media (max-width: 768px) {
    .skill-card {
      width: 150px;
      height: 150px;
    }

    .skill-card i {
      font-size: 3rem;
    }

    .skill-card h3 {
      font-size: 1.2rem;
    }

    .skill-card .level {
      font-size: 0.7rem;
    }
  }
</style>
