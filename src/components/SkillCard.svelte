<script>
  export let skill;
</script>

<div class="skill-card" style="background-color: {skill.color}">
  <img src={skill.icon} alt={skill.name} class="skill-logo" />
</div>

<style>
  .skill-card {
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
    margin: var(--spacing-small);
    transition: transform 0.3s ease;
  }

  .skill-card:hover {
    transform: translateY(-5px);
  }

  .skill-logo {
    width: 50px;
    height: 50px;
    object-fit: contain;
  }
</style>
