<script>
  import ContactSection from "$components/Contact/ContactSection.svelte";
  import ExperienceSection from "$components/Experience/ExperienceSection.svelte";
  import Footer from "$components/Footer/Footer.svelte";
  import IntroSection from "$components/Intro/IntroSection.svelte";
  import ProjectsSection from "$components/Projects/ProjectsSection.svelte";
  import SkillsSection from "$components/Skills/SkillsSection.svelte";
  export let data;
  const { text } = data;
</script>

<head>
  <title>Michael Thomas - Portfolio</title>
  <meta name="description" content="Michael Thomas - Portfolio" />
  <meta name="keywords" content="Michael Thomas, Portfolio" />
  <meta name="author" content="Michael Thomas" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#ffffff" />
  <link rel="icon" type="image/png" href="/favicon.png" />
</head>

<IntroSection />
<SkillsSection />
<ProjectsSection />
<ExperienceSection />
<ContactSection />
<Footer />

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>
