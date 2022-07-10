<script>
  import { Links } from './links.js';
</script>

<h1>Teague Hannam</h1>
{#each Links as i}
  <a href={i.link}>{i.name}</a>
{/each}



<style>
  h1 {
    text-align: right;
    line-height: calc(1rem + 3vw);
    margin: 0;
    font-size: calc(1rem + 3vw);
  }
  a {
    display: block;
    text-align: center;
    font-size: calc(1rem + 3vw);
    line-height: 18vh;
    width: 100%;
  }
  a:hover {
    color: white;
  }
</style>
