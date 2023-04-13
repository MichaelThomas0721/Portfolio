<script>
  import Container from "./Container.svelte";
  import Projects from "$data/projects.json";
  let projects = Projects.projects;
</script>

<div class="min-h-screen flex flex-col items-center gap-6">
  <h3 class="text-5xl font-bold">Projects</h3>
  <div class="flex flex-col gap-8 px-2">
    {#each projects as project, index}
      <Container left={!(index % 2 == 0)} {project} />
    {/each}
  </div>
</div>
