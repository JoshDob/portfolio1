<script>
  import ProjectCard from "./ProjectCard.svelte";
  import projectsData from "./projectsData.js";
</script>

<section class="projects">
  <h2 class="section-title">Projects</h2>
  <div class="projects-grid">
    {#each projectsData as project}
      <ProjectCard {project} />
    {/each}
  </div>
</section>

<style>
  .projects {
    background-color: var(--bg-color);
    color: var(--text-color);
    padding: var(--spacing-large) 0;
    text-align: center;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-large);
    max-width: var(--max-width);
    margin: 0 auto;
    padding: var(--spacing-large) var(--spacing-medium);
  }

  @media (max-width: 768px) {
    .projects-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
