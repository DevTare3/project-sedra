<script lang="ts">
  import { MapPinned } from "lucide-svelte";
</script>

<main class="px-4">
  <h1 class="text-4xl">Gdje se nalazimo?</h1>
  <p>
    Nalazimo se samo minutu od glavne ceste u kovacima<a
      class="hover:text-red-500 transition-all visited:text-black flex gap-2"
      href="https://maps.app.goo.gl/HFMTtyXdTgSUAY4L7"
      target="_blank"
    >
      Kliknite za lokaciju na mapi!<MapPinned />
    </a>
  </p>
</main>
