<script>
  export let info, index;
</script>

<div
  class={`w-full max-w-xl h-2/3 bg-teal text-white order-[${index}] card card-${index} p-3 flex flex-col overflow-hidden`}
>
  <p class="text-left text-4xl">{info.Name}</p>
  <p class="text-3xl">@ {info.Company}</p>
  <p class="text-lg text-gray-300">{info.Start} - {info.End}</p>
  <div class="max-h-32 h-full flex-shrink" />
  <p class="h-fit flex-grow text-lg">
    {info.Description}
  </p>
</div>
