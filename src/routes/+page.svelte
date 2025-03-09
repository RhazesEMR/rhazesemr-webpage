<script>
  import { goto } from "$app/navigation";

  import Button from "$lib/components/ui/button/button.svelte";
  import { Github, Download, Book } from "lucide-svelte";
</script>

<main class="flex flex-grow flex-col items-center mt-32">
  <img class="rounded-md" src="./favicon.png" alt="Logo" width="128" />
  <p class="m-3 text-xl">Rhazes EMR</p>
  <p class="m-3">Modern and User-Friendly Electronic Medical Record</p>

  <div>
    <Button class="text-lg p-5" onclick={() => goto("/download")}
      ><Download />Download</Button
    >
    <Button
      class="text-lg p-5"
      variant="secondary"
      href="https://github.rhazesemr.info"
    >
      <Github /> Source Code</Button
    >
    <Button
      class="text-lg p-5"
      variant="secondary"
      href="https://docs.rhazesemr.info"
    >
      <Book /> Documentation</Button
    >
  </div>
</main>
