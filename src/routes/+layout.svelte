<script>
  import { onMount } from "svelte";

  import "@fortawesome/fontawesome-free/css/all.css";
  import "../app.css";

  import { ModeWatcher } from "mode-watcher";

  import Header from "$lib/share/Header.svelte";
  import Footer from "$lib/share/Footer.svelte";

  let loading = true;

  onMount(() => {
    setTimeout(() => (loading = false), 1000);
  });
</script>

<ModeWatcher />
<main class="flex flex-col min-h-screen">
  {#if loading}
    <div
      class="animate-spin m-auto h-12 w-12 border-4 border-foreground rounded-full border-t-transparent"
    ></div>
  {:else}
    <Header />
    <slot></slot>
    <Footer />
  {/if}
</main>
