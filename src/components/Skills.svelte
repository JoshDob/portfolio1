<script>
  import SkillCard from "./SkillCard.svelte";
  import skillsData from "../data/skillsData";
</script>

<section class="skills">
  <h2 class="section-title">Skills</h2>
  <div class="skill-cards">
    {#each skillsData as skill}
      <SkillCard {skill} />
    {/each}
  </div>
</section>

<style>
  .skills {
    background-color: var(--bg-color);
    color: var(--text-color);
    padding: var(--spacing-large) 0;
    text-align: center;
  }

  .skill-cards {
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacing-medium);
    justify-content: center;
    align-items: center;
    margin-top: var(--spacing-medium);
  }
</style>
