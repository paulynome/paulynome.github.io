<script>
  import { Card, Button } from 'flowbite-svelte';
  import { ArrowRightOutline } from 'flowbite-svelte-icons';
  import capitole from '$lib/assets/capitole_libre_2024.png';
  import green from '$lib/assets/green_evolution.png';
</script>


<h1>Sustainability & Civic Engagement</h1>


<div  class="flex flex-row justify-center my-12 space-x-5">
  <Card img={capitole}>
    <div class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white text-center">Capitole du Libre 2024</div>
    <div class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight text-justify">I volunteered for the organization of the <a href="https://capitoledulibre.org/" class="underline">capitole du libre</a>.</div>
    <!-- <Button color="red">
      Read more <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
    </Button> -->
  </Card>
  <Card img={green} size="xs" imgClass="object-cover h-64 w-96">
    <div class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white text-center">Green Evolution</div>
    <div class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight text-justify">Group project.</div>
    <div class="flex justify-center">
    <Button color="red" href="green_evolution.pdf" class="place-self-center">
      Download
    </Button>
  </div>
  </Card>

</div>
