<script>
  import Card from "./Card.svelte";
  import Contact from "$data/contact.json";
  const icons = Contact.Icons;
</script>

<section class="flex flex-col gap-6">
  <h3 class="text-5xl font-bold text-center">Contact</h3>
  <div class="flex flex-row flex-wrap justify-center gap-6 min-h-[50vh]">
    {#each icons as icon}
      <Card name={icon.Name} icon={icon.Icon} color={icon.Color} href={icon.href} />
    {/each}
  </div>
</section>
