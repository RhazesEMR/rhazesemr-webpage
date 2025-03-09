<script>
  import LdModeSwitch from "./LDModeSwitch.svelte";

  import { goto } from "$app/navigation";

  import { Github } from "lucide-svelte";
  import Button from "$lib/components/ui/button/button.svelte";
</script>

<header
  class="fixed top-0 flex justify-between items-center p-3 w-full bg-background border-b mb-32"
>
  <div class="flex items-center">
    <button on:click={() => goto("/#")}>
      <h1 class="text-2xl font-bold mr-5">
        <i class="fa-solid fa-flask"></i> RhazesEMR
      </h1>
    </button>
    <Button
      onclick={() => (window.location.href = "https://docs.rhazesemr.info")}
      variant="ghost"
    >
      <h1 class="text-lg">Docs</h1>
    </Button>
    <Button onclick={() => goto("/download")} variant="ghost">
      <h1 class="text-lg">Download</h1>
    </Button>
    <Button onclick={() => goto("/features")} variant="ghost">
      <h1 class="text-lg">Features</h1>
    </Button>
    <Button onclick={() => goto("/about")} variant="ghost">
      <h1 class="text-lg">About</h1>
    </Button>
  </div>

  <div class="flex items-center gap-2">
    <a href="https://github.com/RhazesEMR">
      <Button variant="outline" size="icon">
        <Github />
        <span class="sr-only">Github</span>
      </Button>
    </a>
    <LdModeSwitch />
  </div>
</header>
