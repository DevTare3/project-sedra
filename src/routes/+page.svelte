<script lang="ts">
  const images = [
    { src: "/brands/bekament.png", alt: "Bekament" },
    { src: "/brands/knauf.png", alt: "Knauf" },
    { src: "/brands/Philips.png", alt: "Philips" },
    { src: "/brands/rigips.png", alt: "rigips" },
    { src: "/brands/Tarkett.png", alt: "Tarkett" },
  ];
</script>

<div class="bg-slate-300 min-h-screen">
  <h1 class="text-5xl text-center py-10 px-4">
    Sedra za sve vase gradevinske potvrde
  </h1>
</div>
<div class="flex justify-center align-center gap-4 bg-black py-8 px-16">
  {#each images as image}
    <img class="min-w-[4rem] min-h-[4rem]" src={image.src} alt={image.alt} />
  {/each}
</div>
