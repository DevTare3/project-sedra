<script lang="ts">
  import * as Card from "$lib/components/ui/card";
  import * as Carousel from "$lib/components/ui/carousel";
  import type { CarouselAPI } from "$lib/components/ui/carousel/context";
  import Autoplay from "embla-carousel-autoplay";

  const plugin = Autoplay({ delay: 2000, stopOnInteraction: true });
  const images = [
    { src: "/brands/bekament.png", alt: "Bekament" },
    { src: "/brands/knauf.png", alt: "Knauf" },
    { src: "/brands/Philips.png", alt: "Philips" },
    { src: "/brands/rigips.png", alt: "rigips" },
    { src: "/brands/Tarkett.png", alt: "Tarkett" },
  ];

  const examplesOfWork = [
    { src: "/work/1.jpg", alt: "primjer 1" },
    { src: "/work/2.jpg", alt: "primjer 2" },
    { src: "/work/3.jpg", alt: "primjer 3" },
    { src: "/work/4.jpg", alt: "primjer 4" },
    { src: "/work/5.jpg", alt: "primjer 5" },
    { src: "/work/6.jpg", alt: "primjer 6" },
    { src: "/work/7.jpg", alt: "primjer 7" },
    { src: "/work/8.jpg", alt: "primjer 8" },
    { src: "/work/9.jpg", alt: "primjer 9" },
    { src: "/work/10.jpg", alt: "primjer 10" },
    { src: "/work/11.jpg", alt: "primjer 11" },
    { src: "/work/12.jpg", alt: "primjer 12" },
    { src: "/work/13.jpg", alt: "primjer 13" },
    { src: "/work/14.jpg", alt: "primjer 14" },
    { src: "/work/15.jpg", alt: "primjer 15" },
    { src: "/work/16.jpg", alt: "primjer 16" },
  ];

  let api: CarouselAPI;
  let current = 0;
  let count = 0;
  $: if (api) {
    count = api.scrollSnapList().length;
    current = api.selectedScrollSnap() + 1;

    api.on("select", () => {
      current++;
    });
  }
</script>

<div class="bg-blue-500 py-20 min-h-[70vh]">
  <h1 class=" text-2xl lg:text-5xl text-center py-10 px-4 text-white">
    Sedra za sve vase gradevinske potvrde
  </h1>
</div>
<div
  class="text-base text-white text-center sm:text-lg lg:text-2xl md:text-xl bg-black py-4"
>
  <p>Brendovi sa kojima radimo</p>
  <div class="flex justify-center align-center gap-4 bg-black py-8 px-16">
    {#each images as image}
      <img class=" w-16 sm:w-20 md:w-32" src={image.src} alt={image.alt} />
    {/each}
  </div>
</div>
<div class="p-12 w-full flex flex-col items-center justify-center">
  <h1 class="text-4xl text-center mb-8 mt-4">Nasi radovi</h1>
  <div class="flex justify-center items-center flex-col">
    <Carousel.Root
      class="w-full max-w-xl"
      bind:api
      plugins={[plugin]}
      on:mouseenter={plugin.stop}
      on:mouseleave={plugin.reset}
    >
      <Carousel.Content>
        {#each examplesOfWork as work}
          <Carousel.Item>
            <Card.Root>
              <Card.Content class="aspect-square p-0">
                <img
                  class="w-full aspect-square"
                  src={work.src}
                  alt={work.alt}
                />
              </Card.Content>
            </Card.Root>
          </Carousel.Item>
        {/each}
      </Carousel.Content>
      <Carousel.Next />
      <Carousel.Previous />
    </Carousel.Root>
  </div>
  <div class="text-center mt-4">Primjer {current} of {count}</div>
</div>
