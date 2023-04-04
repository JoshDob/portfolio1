<!-- Skills.svelte -->
<script>
  import SkillCard from "./SkillCard.svelte";

  const skills = [
    {
      name: "HTML",
      level: "Expert",
      icon: "fab fa-html5",
    },
    {
      name: "CSS",
      level: "Expert",
      icon: "fab fa-css3-alt",
    },
    {
      name: "JavaScript",
      level: "Advanced",
      icon: "fab fa-js-square",
    },
    // Add more skills as needed
  ];
</script>

<section class="skills">
  <h2>My Skills</h2>
  <div class="skills-container">
    {#each skills as skill}
      <SkillCard
        skillName={skill.name}
        skillLevel={skill.level}
        skillIcon={skill.icon}
      />
    {/each}
  </div>
</section>

<style>
  .skills {
    background-color: var(--bg-color);
    color: var(--text-color);
    padding: var(--spacing-large) var(--spacing-medium);
    text-align: center;
  }

  .skills-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: var(--spacing-medium);
    max-width: 1100px;
    margin: 0 auto;
  }
</style>
