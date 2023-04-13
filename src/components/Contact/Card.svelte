<script>
  export let name, icon, color, href;
</script>

<a
  class="h-44 aspect-square relative flex justify-center items-center rounded-full bg-white group overflow-hidden border-none"
  {href}
  target="_blank"
>
  <img
    src={icon}
    class="w-1/2 aspect-square group-hover:-translate-y-3 transition-default z-30"
    id="icon"
    alt={name + " Icon"}
  />
  <div
    style={`background-color: ${color}`}
    class="absolute h-0 aspect-square rounded-full group-hover:h-[110%] transition-default z-20"
  />
</a>
