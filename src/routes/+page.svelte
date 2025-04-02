<script>
  import { goto } from "$app/navigation";

  import Button from "$lib/components/ui/button/button.svelte";
</script>

<main class="flex flex-grow flex-col items-center mt-64 md:mt-32">
  <img class="rounded-md" src="./favicon.png" alt="Logo" width="128" />
  <p class="m-3 text-xl">Rhazes EMR</p>
  <p class="m-3 text-center">
    Modern and User-Friendly Electronic Medical Record
  </p>

  <div class="flex flex-col md:flex-row">
    <Button class="text-lg m-1 p-5" onclick={() => goto("/download")}
      ><span class="fa-solid fa-download"></span>Download</Button
    >
    <Button
      class="text-lg m-1 p-5"
      variant="secondary"
      href="https://github.rhazesemr.info"
    >
      <span class="fa-solid fa-code-branch"></span>Source Code</Button
    >
    <Button
      class="text-lg m-1 p-5"
      variant="secondary"
      href="https://docs.rhazesemr.info"
    >
      <span class="fa-solid fa-book"></span>Documentation</Button
    >
  </div>
</main>
