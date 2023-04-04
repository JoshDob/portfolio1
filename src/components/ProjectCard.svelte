<script>
  export let project;
</script>

<article class="project-card">
  <img class="project-card__image" src={project.image} alt={project.name} />
  <div class="project-card__details">
    <h3 class="project-card__name">{project.name}</h3>
    <p class="project-card__description">{project.description}</p>
    <ul class="project-card__tech-stack">
      {#each project.techStack as tech}
        <li class="project-card__tech-stack__item">{tech}</li>
      {/each}
    </ul>
    <a class="project-card__link" href={project.url}>View Project</a>
  </div>
</article>

<style>
  .project-card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: var(--spacing-large);
    background-color: var(--bg-color);
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    transition: all 0.3s ease-in-out;
  }

  .project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
  }

  .project-card__image {
    width: 100%;
    height: 180px;
    object-fit: cover;
  }

  .project-card__details {
    padding: var(--spacing-medium);
  }

  .project-card__name {
    font-size: 2rem;
    margin-bottom: var(--spacing-medium);
  }

  .project-card__description {
    font-size: 1.4rem;
    margin-bottom: var(--spacing-medium);
  }

  .project-card__tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacing-small);
    margin-bottom: var(--spacing-medium);
  }

  .project-card__tech-stack__item {
    font-size: 1.2rem;
    font-weight: 500;
    padding: var(--spacing-small) var(--spacing-medium);
    border-radius: 4px;
    background-color: var(--primary-color);
    color: #fff;
  }

  .project-card__link {
    font-size: 1.6rem;
    padding: var(--spacing-small) var(--spacing-medium);
    border-radius: 4px;
    background-color: var(--primary-color);
    color: #fff;
    text-decoration: none;
    transition: all 0.3s ease-in-out;
    display: inline-block;
  }

  .project-card__link:hover,
  .project-card__link:focus {
    background-color: var(--secondary-color);
  }

  .project-card__link:focus::after {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 2px;
    background-color: var(--accent-color);
  }

  @media (max-width: 768px) {
    .project-card__name {
      font-size: 1.8rem;
    }

    .project-card__description {
      font-size: 1.2rem;
    }

    .project-card__tech-stack__item {
      font-size: 1rem;
      padding: var(--spacing-small);
    }

    .project-card__link {
      font-size: 1.4rem;
      padding: var(--spacing-small) var(--spacing-medium);
    }
  }
</style>
