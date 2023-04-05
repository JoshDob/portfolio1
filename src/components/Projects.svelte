<script>
  import ProjectCard from "./ProjectCard.svelte";
  import projectsData from "../data/projectsData.js";
</script>

<div class="section-content section">
  <div class="container">
    <h2 class="section-title">My Projects</h2>
    <div class="projects__grid">
      {#each projectsData as project}
        <ProjectCard
          title={project.title}
          description={project.description}
          imageSrc={project.imageSrc}
          link={project.link}
        />
      {/each}
    </div>
  </div>
</div>

<style>
  .section-content {
    position: relative;
    padding: var(--spacing-medium);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .projects__grid {
    display: grid;
    gap: var(--spacing-large);
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  }

  @media (min-width: 768px) {
    .projects__grid {
      grid-template-columns: repeat(3, 1fr);
    }
  }
</style>
