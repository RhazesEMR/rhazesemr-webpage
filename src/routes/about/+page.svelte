<script>
  import { Info } from "lucide-svelte";
</script>

<main class="flex flex-grow flex-col items-center mt-80 md:mt-32">
  <div class="m-3 text-4xl flex items-center animate-bounce">
    <Info size={52} />
    <p class="px-2">About</p>
    <Info size={52} />
  </div>

  <div>
    <p class="text-lg max-w-3xl text-center p-5">
      RhazesEMR began as a graduation project with the mission to create an
      accessible, open-source electronic medical records system. Named after the
      pioneering Muslim physician Abu Bakr al-Razi, this platform aims to
      provide healthcare professionals with modern tools that respect data
      privacy and security while remaining FOSS and customizable.
    </p>
  </div>
</main>
