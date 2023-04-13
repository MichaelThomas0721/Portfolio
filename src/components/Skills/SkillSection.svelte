<script>
  import SkillsSection from "./SkillsSection.svelte";
  import TextContainer from "./TextContainer.svelte";

    export let skills, activeTxt, className, index, ChangePage Skills, inProgress, ;
</script>

<section
  class={`h-screen overflow-hidden relative flex flex-col gap-3 md:gap-12 justify-between items-center p-3 z-30`}
  id="SkillSection"
>
  <TextContainer {skills} {activeTxt} className="z-30" index={1} />
  <div class="flex flex-row gap-6 z-30 relative mt-auto mr-auto">
    {#each Object.entries(Skills) as [title, content], index}
      <button
        on:click={() => ChangePage(index)}
        class={`px-3 py-2 text-xl rounded-md bg-orange ${
          inProgress ? "bg-opacity-60" : "bg-opacity-10"
        } hover:bg-opacity-20 shadow-xl`}>{title}</button
      >
    {/each}
  </div>
  <clipPath
    class="absolute bottom-0 left-0 aspect-square bg-white z-10 rounded-full flex items-center justify-center overflow-hidden"
    style={`background: ${colors[active]}`}
    id="cover"
  />
    <div
      class="absolute w-full h-full flex flex-col justify-between items-center p-3 z-20"
      id="Cover"
    >
      <TextContainer
        {skills}
        activeTxt={active}
        className="absolute z-30 text-black mx-auto"
        index={2}
      />
      <div class="flex flex-row gap-6 z-30 relative mt-auto mr-auto">
        {#each Object.entries(Skills) as [title, content], index}
          <button
            on:click={() => ChangePage(index)}
            class={`px-3 py-2 text-xl rounded-md bg-orange ${
              inProgress ? "bg-opacity-60" : "bg-opacity-10"
            } hover:bg-opacity-20 shadow-xl`}>{title}</button
          >
        {/each}
      </div>
    </div>
</section>
