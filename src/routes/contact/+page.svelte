<script lang="ts">
  import * as Card from "$lib/components/ui/card";
  import { Phone } from "lucide-svelte";
</script>

<main>
  <Card.Root class="max-w-2xl mx-auto">
    <Card.Header>
      <Card.Title>Kontakt Informacije</Card.Title>
    </Card.Header>
    <Card.Content class="flex gap-2 items-center  ">
      <Phone fill="#333"></Phone>
      <p class="text-left">
        Pozovite nas na: <a
          class="hover:text-red-500 transition-all"
          href="tel:+38761069798">061 069 798</a
        >
      </p>
    </Card.Content>
  </Card.Root>
</main>
