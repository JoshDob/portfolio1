<script>
  export let project;
</script>

<article class="project-card">
  <img src={project.image} alt={project.title} class="project-image" />
  <div class="project-content">
    <h3 class="project-title">{project.title}</h3>
    <p class="project-description">{project.description}</p>
    <div class="project-links">
      <a href={project.live} target="_blank" rel="noopener noreferrer">Live</a>
      <a href={project.github} target="_blank" rel="noopener noreferrer"
        >GitHub</a
      >
    </div>
  </div>
</article>

<style>
  .project-card {
    display: flex;
    flex-direction: column;
    background-color: var(--card-bg-color);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
    border-radius: var(--border-radius);
    overflow: hidden;
  }

  .project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .project-content {
    padding: var(--spacing-medium);
  }

  .project-title {
    font-size: 1.4rem;
    margin-bottom: var(--spacing-small);
  }

  .project-description {
    font-size: 1.2rem;
    line-height: 1.6;
    margin-bottom: var(--spacing-medium);
  }

  .project-links {
    display: flex;
    justify-content: space-between;
  }

  .project-links a {
    font-size: 1.2rem;
    color: var(--text-color);
    text-decoration: none;
  }

  .project-links a:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    .project-image {
      height: 150px;
    }
  }
</style>
