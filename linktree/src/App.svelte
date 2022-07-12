<script>
  import { links } from './Links.js';
</script>

<h1>Teague Hannam</h1>

<main>
  {#each links as i}
    <a href={i.link}>{i.name}</a>
  {/each}
</main>

