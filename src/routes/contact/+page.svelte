<script lang="ts">
  import * as Card from "$lib/components/ui/card";
  import { Phone } from "lucide-svelte";
</script>

<main>
  <Card.Root>
    <Card.Header>
      <Card.Title>Kontakt Informacije</Card.Title>
    </Card.Header>
    <Card.Content>
      <Phone fill="#333"></Phone>
      <p>Pozovite nas na:<a href="tel:+38761069798">061 069 798</a></p>
    </Card.Content>
  </Card.Root>
</main>
