<script>
  import { Button } from "$lib/components/ui/button";
  import * as Card from "$lib/components/ui/card";

  import { toast } from "svelte-sonner";
  import { Download, Github } from "lucide-svelte";

  let win_release = {
    title: "Windows Installer",
    description: "RhazesEMR Desktop Client for Windows",
    msi: "",
    exe: "",
  };

  let mac_release = {
    title: "MacOS Installer",
    description: "RhazesEMR Desktop Client for MacOS",
  };

  let linux_release = {
    title: "Linux Installer",
    description: "RhazesEMR Desktop Client for Linux",
    deb: "",
    rpm: "",
    appimage: "",
  };

  let ios_release = {
    title: "iOS Installer",
    description: "RhazesEMR Mobile Client for iOS",
  };

  let android_release = {
    title: "Android Installer",
    description: "RhazesEMR Mobile Client for Android",
    apk: "",
  };

  let github_release = "https://github.com/RhazesEMR/rhazesemr-client/releases";
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
        <Card.Title>{win_release.title}</Card.Title>
        <Card.Description>{win_release.description}</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pb-4">
          <i class="animate-pulse fa-brands fa-windows text-9xl"></i>
        </div>
        <!-- <div class="flex flex-grow justify-center"> <Button class="w-1/2 mr-1" href={win_release.exe}> <Download /> EXE </Button> <Button class="w-1/2" href={win_release.msi}> <Download /> MSI </Button> </div> -->
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>Coming soon...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary" href={github_release}
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>{android_release.title}</Card.Title>
        <Card.Description>{android_release.description}</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-4">
          <i class="animate-pulse fa-brands fa-android text-9xl"></i>
        </div>
        <!-- <Button class="w-full" href={android_release.apk}> <Download /> APK </Button> -->
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>Coming soon...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary" href={github_release}
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>{linux_release.title}</Card.Title>
        <Card.Description>{linux_release.description}</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="animate-pulse fa-brands fa-linux text-9xl"></i>
        </div>
        <!-- <div class="flex flex-grow justify-center"> <Button class="w-1/3 mr-1" href={linux_release.deb}> <Download /> DEB </Button> <Button class="w-1/3 mr-1" href={linux_release.rpm}> <Download /> RPM </Button> <Button class="w-1/3" href={linux_release.appimage}> <Download /> AppImage </Button> </div> -->
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>Coming soon...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary" href={github_release}
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>{mac_release.title}</Card.Title>
        <Card.Description>{mac_release.description}</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="animate-pulse fa-brands fa-apple text-9xl"></i>
        </div>
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>Coming soon...</Button>
        </button>
      </Card.Content>
      <Card.Footer>
        <Button class="w-full" variant="secondary" href={github_release}
          ><Github /> Github Release</Button
        >
      </Card.Footer>
    </Card.Root>

    <Card.Root class="w-[380px] m-2">
      <Card.Header>
        <Card.Title>{ios_release.title}</Card.Title>
        <Card.Description>{ios_release.description}</Card.Description>
      </Card.Header>
      <Card.Content class="grid gap-4">
        <div class="flex justify-center pt-2 pb-2">
          <i class="animate-pulse fa-brands fa-apple text-9xl"></i>
        </div>
        <button
          onclick={() =>
            toast.warning("Not available yet", {
              description: "this release is still in need for further testing",
            })}
        >
          <Button class="w-full" disabled>Coming soon...</Button>
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
