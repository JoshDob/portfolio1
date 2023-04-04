<script>
</script>

<section class="about" id="about">
  <div class="container">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-text">
        <p>
          Hello! I'm Joshua Dobrowner, a passionate full-stack web developer
          with experience in various technologies and a focus on creating
          efficient, user-friendly web applications. I enjoy tackling new
          challenges and learning new technologies to improve my skillset.
        </p>
        <p>
          When I'm not coding, I enjoy spending time outdoors, traveling, and
          trying new foods.
        </p>
      </div>
      <div class="about-image">
        <img
          src="https://via.placeholder.com/300/444444/ffffff?text=Your+Image"
          alt="Joshua Dobrowner"
        />
      </div>
    </div>
  </div>
</section>

<style>
  .about {
    position: relative;
    padding: var(--spacing-large) 0;
    background-color: var(--bg-color);
    color: var(--text-color);
  }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 var(--spacing-medium);
    text-align: center;
  }

  .about-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: var(--spacing-large);
  }

  .about-text {
    font-size: 1.6rem;
    line-height: 1.5;
    max-width: 600px;
  }

  .about-image {
    width: 300px;
    height: 300px;
    overflow: hidden;
    border-radius: 50%;
  }

  .about-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  @media (max-width: 768px) {
    .about-text {
      font-size: 1.4rem;
    }

    .about-image {
      width: 250px;
      height: 250px;
    }
  }
</style>
