<script>
  import AnimatedWave from "./AnimatedWave.svelte";
</script>

<section class="about">
  <div class="wave-container">
    <AnimatedWave />
  </div>
  <div class="container">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-text">
        <p>
          Hi, I'm Joshua Dobrowner, a full-stack web developer with a passion
          for creating efficient and user-friendly web applications. I have
          experience in HTML, CSS, JavaScript, and various modern web
          development frameworks and libraries.
        </p>
        <p>
          When I'm not coding, I enjoy outdoor activities, such as hiking and
          cycling, as well as playing guitar and exploring new music.
        </p>
      </div>
      <img
        src="/images/joshua_dobrowner.jpg"
        alt="Joshua Dobrowner"
        class="about-image"
      />
    </div>
  </div>
</section>

<style>
  .about {
    position: relative;
    background-color: var(--bg-color);
    color: var(--text-color);
    padding: var(--spacing-large) var(--spacing-medium);
  }

  .wave-container {
    position: relative;
    overflow: visible;
  }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    text-align: center;
  }

  .about-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: var(--spacing-large);
    margin-top: var(--spacing-large);
  }

  .about-text {
    flex: 1;
    max-width: 600px;
    font-size: 1.4rem;
    line-height: 1.6;
    text-align: left;
  }

  .about-image {
    width: 300px;
    height: 300px;
    object-fit: cover;
    border-radius: 50%;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
  }

  @media (max-width: 768px) {
    .about-text {
      font-size: 1.2rem;
    }

    .about-image {
      width: 250px;
      height: 250px;
    }
  }
</style>
