<script>
  import LdModeSwitch from "./LDModeSwitch.svelte";

  import { goto } from "$app/navigation";

  import { Github } from "lucide-svelte";
  import Button from "$lib/components/ui/button/button.svelte";
</script>

<header
  class="fixed top-0 flex flex-col md:flex-row justify-between items-center p-3 w-full bg-background border-b mb-32"
>
  <div class="flex flex-col md:flex-row items-center mb-1 md:mb-0">
    <button on:click={() => goto("/#")}>
      <h1 class="text-2xl font-bold mr-5">
        <i class="fa-solid fa-flask"></i> RhazesEMR
      </h1>
    </button>
    <Button href="https://docs.rhazesemr.info" variant="link">
      <h1 class="text-lg">Docs</h1>
    </Button>
    <Button onclick={() => goto("/download")} variant="link">
      <h1 class="text-lg">Download</h1>
    </Button>
    <Button onclick={() => goto("/features")} variant="link">
      <h1 class="text-lg">Features</h1>
    </Button>
    <Button onclick={() => goto("/about")} variant="link">
      <h1 class="text-lg">About</h1>
    </Button>
  </div>

  <div class="flex items-center gap-2">
    <Button
      variant="outline"
      size="icon"
      href="https://bsky.app/profile/rhazesemr.bsky.social"
    >
      <i class="fa-brands fa-bluesky"></i>
      <span class="sr-only">Bluesky</span>
    </Button>
    <Button variant="outline" size="icon" href="https://github.com/RhazesEMR">
      <Github />
      <span class="sr-only">Github</span>
    </Button>
    <LdModeSwitch />
  </div>
</header>
