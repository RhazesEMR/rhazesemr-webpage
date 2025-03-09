<script>
  import * as Card from "$lib/components/ui/card";

  import { Sparkles } from "lucide-svelte";

  const features = [
    {
      title: "Patient Records Management",
      description:
        "Effortlessly manage comprehensive patient information in one secure location. Track medical histories, store diagnostic results, and access patient data instantly with our intuitive interface designed for healthcare professionals.",
    },
    {
      title: "Cross-Platform Compatibility",
      description:
        "Access Rhazes EMR from any device and operating system. Our Tauri-based application delivers native performance while maintaining a consistent and responsive experience across all platforms.",
    },
    {
      title: "Open Source",
      description:
        "Built as Free and Open Source Software (FOSS), Rhazes EMR gives you complete freedom from vendor lock-in. Customize the platform to your specific needs, contribute to development, and benefit from community innovations.",
    },
    {
      title: "Security-First Architecture",
      description:
        "Protect sensitive patient data with our security-focused design. Our isolated database containers, encrypted connections, and role-based access controls ensure patient information remains private and secure.",
    },
    {
      title: "Modern User Interface",
      description:
        "Experience healthcare software designed for humans. Our Svelte and TailwindCSS interface reduces cognitive load and training time, allowing healthcare professionals to focus on patients rather than software.",
    },
    {
      title: "Built-in AI Assistant",
      description:
        "Enhance clinical workflows with our integrated Saba AI assistant. Powered by Mistral's specialized 24B parameter model, this Arabic-fluent chatbot understands regional nuances and medical terminology to provide culturally relevant support for Middle Eastern healthcare contexts.",
    },
    {
      title: "Easy Deployment",
      description:
        "Get up and running quickly with our Docker-based deployment. The simple docker-compose file automatically configures both the database and API, making installation and maintenance straightforward even for non-technical users.",
    },
    {
      title: "Analytics & Reporting",
      description:
        "Make data-driven decisions with customizable clinical reports and practice analytics. Gain insights into patient populations, track quality metrics, and optimize your practice with our powerful reporting tools.",
    },
  ];
</script>

<main class="flex flex-col items-center mt-28">
  <div class="m-3 text-4xl flex items-center animate-bounce">
    <Sparkles size={52} />
    <p class="px-2">Features</p>
    <Sparkles size={52} />
  </div>

  <p class="text-lg">RhazesEMR features & capabilities</p>

  <div class="flex flex-wrap justify-center mt-10 max-w-3xl">
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
  </div>
</main>
