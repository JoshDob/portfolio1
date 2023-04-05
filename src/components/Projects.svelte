<script>
  import ProjectCard from "./ProjectCard.svelte";
  import projectsData from "../data/projectsData.js";
</script>

<section class="projects">
  <div class="projects-content">
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
</section>

<style>
  .projects {
    padding: var(--spacing-large) 0;
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
