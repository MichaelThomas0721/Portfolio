<script>
  import RiSystemArrowDownSLine from "svelte-icons-pack/ri/RiSystemArrowDownSLine";
  import FiArrowDown from "svelte-icons-pack/fi/FiArrowDown";
  import Icon from "svelte-icons-pack/Icon.svelte";
  import "$styles/BounceButton.scss";
</script>

<section
  class="flex flex-col gap-2 items-center min-h-[850px] w-full justify-around bg-gradient-to-b from-teal to-darkTeal p-3"
  id="intro"
>
  <div class="flex flex-row flex-wrap gap-2 justify-around w-full items-center">
    <div class="flex flex-col gap-1">
      <p class="text-4xl">Hello! My name is</p>
      <h1 class="text-5xl font-bold">Michael Thomas</h1>
      <h2 class="text-4xl">Full Stack Developer</h2>
    </div>
    <img
      src="ProfilePicture.jpg"
      class="w-96 aspect-square rounded-full bg-white object-cover"
      alt="Profile Picture"
    />
  </div>
  <a
    href="/resume.pdf"
    class="bg-orange hover:bg-opacity-80 p-3 px-6 font-semibold text-2xl rounded-sm"
    >View My Resume</a
  >
  <a href="#SkillSection"
    class="w-16 aspect-square flex justify-center items-center group text-white"
    ><Icon
      src={RiSystemArrowDownSLine}
      className="text-6xl h-fit w-fit group-hover:scale-150 transition-all duration-300 button-bounce"
      ><linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" style="stop-color:#f00;stop-opacity:1" />
        <stop
          offset="100%"
          style="stop-color:#00f;stop-opacity:1"
        /></linearGradient
      ></Icon
    ></a
  >
</section>
