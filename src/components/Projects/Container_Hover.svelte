<script>
    export let left;
</script>

<div class={`w-20 group-hover:w-0 flex-shrink-0 transition-all duration-300 overflow-hidden flex flex-col justify-between ${left ? 'items-start' : 'items-end'}`}>
    <div class={`z-10 w-12 h-12 aspect-square bg-teal rounded-full absolute bottom-6 ${left ? 'left-6 group-hover:left-0 group-hover:-translate-x-[15%]' : 'right-6 group-hover:right-0 group-hover:translate-x-[15%]'} group-hover:w-[650px] group-hover:h-[650px] group-hover:bg-opacity-50 group-hover:bottom-0 group-hover:translate-y-1/4 transition-all duration-300`} />
    <h3 class="text-3xl font-bold text-white text-vertical">
      Hover Me!
    </h3>
  </div>