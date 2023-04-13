<script>
  export let name, icon, color;
</script>

<div
  class="h-44 aspect-square relative flex justify-center items-center rounded-full bg-white group overflow-hidden border-none"
>
  <a
    id="Icon"
    class="w-1/2 aspect-square group-hover:-translate-y-3 transition-default z-30"
  >
    <img src={icon} class="w-full" alt={name + " Icon"} />
  </a>
  <div
    style={`background-color: ${color}`}
    class="absolute h-0 aspect-square rounded-full group-hover:h-[110%] transition-default z-20"
  />
</div>
