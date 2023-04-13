<script>
  import Card from "./Card.svelte";
  import Contact from "$data/contact.json";
  const icons = Contact.Icons;
</script>

<div>
  <p>Contact</p>
  <div class="flex flex-row flex-wrap justify-center gap-6 min-h-[50vh]">
    {#each icons as icon}
      <Card name={icon.Name} icon={icon.Icon} color={icon.Color} />
    {/each}
  </div>
</div>
