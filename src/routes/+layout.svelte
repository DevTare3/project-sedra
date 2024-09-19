<script lang="ts">
  import { Button } from "$lib/components/ui/button";
  import {base} from "$app/paths";
  import "../app.css";
</script>

<header>
  <nav class="lg:px-12 lg:py-6 flex justify-between items-center px-4 py-3">
    <div class="w-8 sm:w-12 md:w-16">
      <img src="/sedra-logo.svg" alt="the logo of the company" />
    </div>
    <ul>
      <Button href="{base}" variant="link" class="px-2 py-2 text-base"
        >Pocetna</Button
      >
      <Button href="{base}/contact" variant="link" class="px-2 py-2 text-base"
        >Kontakt</Button
      >
      <Button variant="link" href="{base}/location" class="px-2 py-2 text-base"
        >Lokacija</Button
      >
    </ul>
  </nav>
</header>
<main>
  <slot></slot>
</main>
