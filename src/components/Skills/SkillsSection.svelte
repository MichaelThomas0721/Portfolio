<script>
  import Skills from "$data/skills.json";
  import "$styles/SkillPage.scss";
  import TextContainer from "./TextContainer.svelte";
  // @ts-ignore
  const { FrontEnd, BackEnd, Other } = Skills;
  const skills = [FrontEnd, BackEnd, Other];
  const colors = [FrontEnd.Color, BackEnd.Color, Other.Color];
  let active = 0;
  let activeTxt = 0;
  let cover;
  let main;
  let text;
  let inProgress = false;
  function ChangePage(index) {
    if (inProgress) return;
    if (cover) {
      inProgress = true;
      cover.classList.add("cover-anim");
      active = index;
      setTimeout(() => {
        cover.classList.remove("cover-anim");
        activeTxt = index;
        main.style.background = colors[active];
        inProgress = false;
      }, 1000);
    } else {
      cover = document.getElementById("Skills_TextContainer2");
      main = document.getElementById("SkillSection");
      text = document.getElementById("Skills_TextContainer1");
      ChangePage(index);
      return;
    }
    return;
  }
</script>

<section
  class={`min-h-[850px] h-fit overflow-hidden relative flex flex-col gap-3 md:gap-12 justify-between items-center z-30`}
  id="SkillSection"
>
  <TextContainer
    {skills}
    {activeTxt}
    className="z-30 px-2"
    index={1}
    background={null}
  />
  <TextContainer
    {skills}
    activeTxt={active}
    className="absolute z-30 w-screen h-screen px-4"
    background={colors[active]}
    index={2}
  />
  <div class="flex flex-row gap-6 z-50 absolute bottom-6 left-6">
    {#each Object.entries(Skills) as [title, content], index}
      <button
        on:click={() => ChangePage(index)}
        class={`px-3 py-2 text-xl rounded-md bg-orange ${
          inProgress ? "bg-opacity-60" : "bg-opacity-10"
        } hover:bg-opacity-20 shadow-xl`}>{title}</button
      >
    {/each}
  </div>
</section>
