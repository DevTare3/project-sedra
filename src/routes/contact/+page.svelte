<script lang="ts">
  import * as Card from "$lib/components/ui/card";
  import { Phone } from "lucide-svelte";
</script>

<main>
  <Card.Root class="max-w-2xl mx-auto">
    <Card.Header>
      <Card.Title>Kontakt Informacije</Card.Title>
    </Card.Header>
    <Card.Content
      class="flex flex-row-reverse gap-2 items-center text-left pr-16 "
    >
      <Phone fill="#333"></Phone>
      <p class="">
        Pozovite nas na: <a
          class="hover:text-red-500 transition-all"
          href="tel:+38761069798">061 069 798</a
        >
      </p>
    </Card.Content>
  </Card.Root>
</main>
