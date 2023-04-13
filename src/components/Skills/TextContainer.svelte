<script>
    export let skills, activeTxt, className, index, background;
</script>

<div id={"Skills_TextContainer" + index} class={`${className}`} style={background ? `background: ${background}` : ''}>
    <h3 class="text-6xl relative z-30 text-center pt-16">
      {skills[activeTxt].Title}
    </h3>
    <div class="z-30 relative w-fit mx-auto flex flex-col gap-3 md:gap-8">
      {#each Object.entries(skills[activeTxt].Skills) as [title, content], index}
        <div class="flex flex-col gap-4">
          <h1 class="text-2xl">{title}</h1>
          <div class="flex flex-row flex-wrap gap-4">
            {#each content as skill}
              <div class="flex flex-col gap-2">
                <div class="flex flex-row gap-2">
                  <div class="w-6 h-6 rounded-full bg-orange" />
                  <p>{skill}</p>
                </div>
                <div class="w-full h-1 bg-orange" />
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </div>