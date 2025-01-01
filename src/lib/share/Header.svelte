<script>
  import LdModeSwitch from "./LDModeSwitch.svelte";

  import { goto } from "$app/navigation";

  import { Github } from "lucide-svelte";
  import Button from "$lib/components/ui/button/button.svelte";
</script>

<header
  class="fixed top-0 flex justify-between p-3 w-full bg-background border-b"
>
  <button onclick={() => goto("/#")}>
    <h1 class="text-xl">
      <i class="fa-solid fa-flask"></i> RhazesEMR
    </h1>
  </button>

  <div>
    <a href="https://github.com/RhazesEMR">
      <Button variant="outline" size="icon">
        <Github />
        <span class="sr-only">Github</span>
      </Button>
    </a>
    <LdModeSwitch />
  </div>
</header>
