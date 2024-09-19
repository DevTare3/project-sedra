<script lang="ts">
  import { MapPinned } from "lucide-svelte";
</script>

<main class="px-4 bg-blue-500 min-h-screen text-center py-8">
  <h1 class="text-4xl mb-4">Gdje se nalazimo?</h1>
  <p class="text-center">
    Nalazimo se samo minutu od glavne ceste u kovacima<a
      class="hover:text-blue-800 transition-all visited:text-white flex gap-2 text-white items-center justify-center"
      href="https://maps.app.goo.gl/HFMTtyXdTgSUAY4L7"
      target="_blank"
    >
      Kliknite za lokaciju na mapi!<MapPinned />
    </a>
  </p>
</main>
