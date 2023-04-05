<script>
  import SkillCard from "./SkillCard.svelte";
  import skillsData from "../data/skillsData";
</script>

<div class="section-content section">
  <h2 class="section-title">Skills</h2>
  <div class="skill-cards">
    {#each skillsData as skill}
      <SkillCard {skill} />
    {/each}
  </div>
</div>

<style>
  .section-content {
    position: relative;
    padding: var(--spacing-medium);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
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
