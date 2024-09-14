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
  <h1 class="text-5xl text-center py-10">
    Sedra za sve vase gradevinske potvrde
  </h1>
  <div class="flex justify-center align-center gap-4">
    {#each images as image}
      <img class=" w-32" src={image.src} alt={image.alt} />
    {/each}
  </div>
</div>
