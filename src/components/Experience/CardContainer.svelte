<script>
  import Card from "./Card.svelte";
  import Experience from "$data/experience.json";
  import RiSystemArrowDownSLine from "svelte-icons-pack/ri/RiSystemArrowDownSLine";
  import RiSystemArrowUpSLine from "svelte-icons-pack/ri/RiSystemArrowUpSLine";
  import Icon from "svelte-icons-pack/Icon.svelte";
  const jobs = Experience.jobs;
  let indexes = [-1, 0, 1, 2, 3, 4];
  let colors = ["red", "green", "blue"];

  function MoveDown() {
    let tempIndex = indexes[0];
    for (let i = 0; i < indexes.length - 1; i++) {
      indexes[i] = indexes[i + 1];
    }
    indexes[indexes.length - 1] = tempIndex;
  }

  function MoveUp() {
    let tempIndex = indexes[indexes.length - 1];
    for (let i = indexes.length - 1; i > 0; i--) {
      indexes[i] = indexes[i - 1];
    }
    indexes[0] = tempIndex;
  }
</script>

<div class="h-full w-full flex flex-col justify-center items-center px-2">
  <button on:click={MoveUp}
    ><Icon
      src={RiSystemArrowUpSLine}
      size="64"
      className="w-fit h-fit fill-white"
    /></button
  >
  <div
    class="flex flex-col justify-center items-center gap-3 card-container h-[60vh] w-full p-2 relative"
  >
    {#each jobs as job, index}
      <Card
        info={job}
        index={indexes[index]}
        color={colors[index >= 3 ? index - 3 : index]}
      />
    {/each}
    {#each jobs as job, index}
      <Card info={job} index={indexes[index + 3]} color={colors[index]} />
    {/each}
  </div>
  <button on:click={MoveDown}
    ><Icon
      src={RiSystemArrowDownSLine}
      size="64"
      className="w-fit h-fit fill-white"
    /></button
  >
</div>
