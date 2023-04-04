<script>
  import { FontAwesomeIcon } from "@fortawesome/svelte-fontawesome";
  import { faEnvelope } from "@fortawesome/free-solid-svg-icons";
  import { faLinkedin, faGithub } from "@fortawesome/free-brands-svg-icons";
</script>

<section class="contact">
  <h2 class="section-title">Contact Me</h2>
  <div class="contact-links">
    <div class="contact-link">
      <a
        href="https://github.com/YourUsername"
        target="_blank"
        rel="noopener noreferrer"
      >
        <FontAwesomeIcon icon={faGithub} class="contact-icon" />
        <span class="sr-only">Github</span>
      </a>
      <p>Github</p>
    </div>
    <div class="contact-link">
      <a
        href="https://www.linkedin.com/in/yourlinkedinprofile/"
        target="_blank"
        rel="noopener noreferrer"
      >
        <FontAwesomeIcon icon={faLinkedin} class="contact-icon" />
        <span class="sr-only">LinkedIn</span>
      </a>
      <p>LinkedIn</p>
    </div>
    <div class="contact-link">
      <a
        href="mailto:youremail@example.com"
        target="_blank"
        rel="noopener noreferrer"
      >
        <FontAwesomeIcon icon={faEnvelope} class="contact-icon" />
        <span class="sr-only">Email</span>
      </a>
      <p>Email</p>
    </div>
  </div>
</section>

<style>
  .contact {
    background-color: var(--bg-color);
    color: var(--text-color);
    padding: var(--spacing-large) 0;
    text-align: center;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    max-width: var(--max-width);
    margin: 0 auto;
    gap: var(--spacing-medium);
  }

  .contact-link {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .contact-icon {
    font-size: 2rem;
    margin-bottom: var(--spacing-small);
  }

  .sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    border: 0;
  }

  @media (max-width: 768px) {
    .contact-links {
      flex-direction: column;
    }

    .contact-link {
      margin: var(--spacing-medium) 0;
    }
  }
</style>
