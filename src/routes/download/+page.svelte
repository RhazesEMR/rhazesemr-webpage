<script>
  import { Button } from "$lib/components/ui/button";
  import * as Card from "$lib/components/ui/card";

  import { toast } from "svelte-sonner";
  import { Download, Github } from "lucide-svelte";
</script>

<main class="flex flex-grow flex-col items-center mt-28">
  <div class="m-3 text-4xl flex items-center animate-bounce">
    <Download size={52} />
    <p class="px-2">Download</p>
    <Download size={52} />
  </div>

  <p class="text-lg">Download the latest version of RhazesEMR</p>

  <div class="flex flex-wrap justify-center mt-5">
    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>Windows Installer</Card.Title>
        <Card.Description>RhazesEMR Desktop Client for Windows</Card.Description
        >
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pb-4">
          <i class="fa-brands fa-windows text-9xl"></i>
        </div>

        <div class="flex flex-grow justify-center">
          <Button class="w-1/2 mr-1">
            <Download /> EXE
          </Button>
          <Button class="w-1/2">
            <Download /> MSI
          </Button>
        </div>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary"
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>Android Installer</Card.Title>
        <Card.Description>RhazesEMR Mobile Client for Android</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-4">
          <i class="fa-brands fa-android text-9xl"></i>
        </div>
        <Button class="w-full">
          <Download /> APK
        </Button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary"
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>Linux Installer</Card.Title>
        <Card.Description
          >RhazesEMR Desktop Client for GNU/Linux</Card.Description
        >
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="fa-brands fa-linux text-9xl"></i>
        </div>
        <div class="flex flex-grow justify-center">
          <Button class="w-1/3 mr-1">
            <Download /> DEB
          </Button>
          <Button class="w-1/3 mr-1">
            <Download /> RPM
          </Button>
          <Button class="w-1/3">
            <Download /> AppImage
          </Button>
        </div>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary"
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>MacOS Installer</Card.Title>
        <Card.Description>RhazesEMR Desktop Client for MacOS</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="fa-brands fa-apple text-9xl"></i>
        </div>
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary"
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>iOS Installer</Card.Title>
        <Card.Description>RhazesEMR Mobile Client for iOS</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="fa-brands fa-apple text-9xl"></i>
        </div>
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary"
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>
  </div>
</main>
