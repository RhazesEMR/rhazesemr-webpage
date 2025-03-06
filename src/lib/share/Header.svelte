<script>
  import LdModeSwitch from "./LDModeSwitch.svelte";

  import { goto } from "$app/navigation";

  import { Github } from "lucide-svelte";
  import Button from "$lib/components/ui/button/button.svelte";
</script>

<header class="fixed top-0 flex justify-between items-center p-3 w-full bg-background border-b">
  <div class="flex items-center gap-4">
    <button on:click={() => goto("/#")}>
      <h1 class="text-xl">
        <i class="fa-solid fa-flask"></i> RhazesEMR
      </h1>
    </button>
    <button on:click={() => window.location.href = "https://docs.rhazesemr.info"}>
      <h1 class="text-lg">
        Docs
      </h1>
    </button>
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
