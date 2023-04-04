<script>
  export let title;
  export let description;
  export let imageSrc;
  export let link;
</script>

<div class="project-card">
  <img src={imageSrc} alt="Project image" class="project-card__image" />
  <div class="project-card__info">
    <h3 class="project-card__title">{title}</h3>
    <p class="project-card__description">{description}</p>
    <a href={link} class="project-card__link">View Project</a>
  </div>
</div>

<style>
  .project-card {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    overflow: hidden;
    transition: transform 0.3s ease;
    width: 100%;
  }

  .project-card__image {
    height: 100%;
    object-fit: cover;
    object-position: center;
    width: 100%;
  }

  .project-card__info {
    padding: 1rem;
  }

  .project-card__title {
    font-size: 1.5rem;
    margin-bottom: 0.5rem;
  }

  .project-card__description {
    margin-bottom: 1rem;
  }

  .project-card__link {
    color: var(--accent-color);
    font-weight: bold;
    transition: color 0.3s ease;
  }

  .project-card__link:hover {
    color: var(--primary-color);
  }
</style>
