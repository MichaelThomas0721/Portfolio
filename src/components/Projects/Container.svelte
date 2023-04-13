<script>
  import "$styles/ProjectCard.scss";
  import ContainerHover from "./Container_Hover.svelte";
  export let left;
  export let project;
  let { Name, Description, Tags, Image, Link } = project;
</script>

<div class="max-w-[850px] w-full h-[400px] bg-midTeal rounded-xl p-3 relative flex flex-row justify-between group overflow-hidden">
    {#if left}
    <ContainerHover { left } />
    {/if}
    <div class="relative h-full flex-grow rounded-xl overflow-hidden transition-all duration-300 grayscale group-hover:grayscale-0">
      <img
        src={Image}
        class="object-cover h-full w-full"
        alt="project"
      />
    </div>
    <div class={`absolute bottom-8 ${left ? 'left-24 group-hover:left-6 text-left items-start' : 'right-24 group-hover:right-6 text-right items-end'} z-20 flex flex-col gap-2 transition-all duration-300`}>
      <p class="text-5xl font-extrabold z-20">
        {Name}
      </p>
      <p class="w-96 max-h-0 group-hover:max-h-96 overflow-hidden transition-all duration-300 z-20">
        {Description}
      </p>
      <ul class="flex flex-row gap-2">
        {#each Tags as tag}
            <li class="transition-all duration-300 max-h-0 group-hover:max-h-8 p-1 px-2 overflow-hidden bg-green-500 rounded-md">
              {tag}
            </li>
        {/each}
      </ul>
    </div>
    {#if !left}
    <ContainerHover { left } />
    {/if}
  </div>