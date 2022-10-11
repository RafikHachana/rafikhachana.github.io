<script lang="ts">
  import type {Project} from '$lib/types';
  import Intro from '$lib/Intro.svelte';
  import Skills from '$lib/Skills.svelte';
  import Experience from '$lib/Experience.svelte';
  import { experience, skills, intro_content } from '$lib/data';

  let projects: Project[] = experience;

</script>

<svelte:head>
  <title>Rafik's portfolio</title>
  <link rel="icon" type="image/x-icon" href="/favicon.ico">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,500;0,700;1,300&display=swap" rel="stylesheet"> 
</svelte:head>


<Intro content={intro_content}/>
<Skills {skills} />

