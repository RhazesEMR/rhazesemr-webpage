<script>
  import { goto } from "$app/navigation";

  import Button from "$lib/components/ui/button/button.svelte";

  import * as Card from "$lib/components/ui/card";

  import { Sparkles, ExternalLink } from "lucide-svelte";

  const features = [
    {
      title: "Patient Records Management",
      description:
        "Effortlessly manage comprehensive patient information in one secure location. Track medical histories, store diagnostic results, and access patient data instantly with our intuitive interface designed for healthcare professionals.",
    },
    {
      title: "Security-First Architecture",
      description:
        "Protect sensitive patient data with our security-focused design. Our isolated database containers, encrypted connections, and role-based access controls ensure patient information remains private and secure.",
    },
    {
      title: "Built-in AI Assistant",
      description:
        "Enhance clinical workflows with our integrated Saba AI assistant. Powered by Mistral's specialized 24B parameter model, this Arabic-fluent chatbot understands regional nuances and medical terminology to provide culturally relevant support for Middle Eastern healthcare contexts.",
    },
  ];
</script>

<main class="flex flex-grow flex-col items-center">
  <div
    class="w-full h-full bg-fixed relative bg-cover bg-center"
    style="background-image: url('./banner.jpg');"
  >
    <div
      class="flex flex-grow flex-col items-center pt-64 md:pt-24 pb-3 md:pb-8 backdrop-brightness-50 backdrop-blur-sm"
    >
      <img class="rounded-md" src="./favicon.png" alt="Logo" width="128" />
      <p class="m-3 text-xl text-white">Rhazes EMR</p>
      <p class="m-3 text-center text-white">
        Modern and User-Friendly Electronic Medical Record
      </p>

      <div class="flex flex-col md:flex-row">
        <Button class="text-lg m-1 p-5" onclick={() => goto("/download")}
          ><span class="fa-solid fa-download"></span>Download</Button
        >
        <Button
          class="text-lg m-1 p-5"
          variant="secondary"
          href="https://git.rhazesemr.info"
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
    </div>
  </div>

  <div class="m-3 mt-10 text-4xl flex items-center">
    <Sparkles size={52} />
    <p class="px-2">Features</p>
    <Sparkles size={52} />
  </div>

  <div class="flex flex-wrap justify-center mt-5 max-w-4xl">
    {#each features as feature}
      <Card.Root class="m-2">
        <Card.Content class="flex">
          <div class="">
            <h1 class="mb-5 text-3xl">{feature.title}</h1>
            <p>{feature.description}</p>
          </div>
        </Card.Content>
      </Card.Root>
    {/each}
    <Button variant="link" onclick={() => goto("/features")}
      >See more<ExternalLink />
    </Button>
  </div>
</main>
