<script lang="ts">
  import { Button } from "$lib/components/ui/button";
  import "../app.css";
</script>

<header>
  <nav class="px-7 py-6 flex justify-between items-center">
    <div class="">Sedra</div>
    <ul>
      <Button href="/" variant="link" class="px-2 py-2 text-base"
        >Pocetna</Button
      >
      <Button href="/contact" variant="link" class="px-2 py-2 text-base"
        >Kontakt</Button
      >
      <Button href="/location" variant="link" class="px-4 py-2 text-base"
        >Lokacija</Button
      >
    </ul>
  </nav>
</header>

<slot></slot>
