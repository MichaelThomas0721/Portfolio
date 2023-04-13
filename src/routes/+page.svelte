<script>
  import ContactSection from "$components/Contact/ContactSection.svelte";
import ExperienceSection from "$components/Experience/ExperienceSection.svelte";
import IntroSection from "$components/Intro/IntroSection.svelte";
  import ProjectsSection from "$components/Projects/ProjectsSection.svelte";
  import SkillsSection from "$components/Skills/SkillsSection.svelte";
  export let data;
  const { text } = data;
</script>

<div class="">
  <IntroSection />
  <SkillsSection />
  <ProjectsSection />
  <ExperienceSection />
  <ContactSection />
</div>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>
