<script>
  import ProjectCard from "./ProjectCard.svelte";

  const projects = [
    {
      name: "Project 1",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed at lorem quis eros tempus consequat.",
      image: "https://via.placeholder.com/500x300/444444/ffffff?text=Project+1",
      url: "#",
      techStack: ["HTML", "CSS", "JavaScript"],
    },
    {
      name: "Project 2",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed at lorem quis eros tempus consequat.",
      image: "https://via.placeholder.com/500x300/444444/ffffff?text=Project+2",
      url: "#",
      techStack: ["React", "Node.js", "MongoDB"],
    },
    {
      name: "Project 3",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed at lorem quis eros tempus consequat.",
      image: "https://via.placeholder.com/500x300/444444/ffffff?text=Project+3",
      url: "#",
      techStack: ["Vue", "Firebase", "Tailwind CSS"],
    },
  ];
</script>

<section class="projects">
  <h2>My Projects</h2>
  <div class="projects-container">
    {#each projects as project}
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

  .projects h2 {
    font-size: 3rem;
    margin-bottom: var(--spacing-medium);
  }

  .projects-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: var(--spacing-medium);
    max-width: var(--max-width);
    margin: 0 auto;
  }

  @media (max-width: 768px) {
    .projects-container {
      flex-direction: column;
      gap: var(--spacing-large);
    }
  }
</style>
