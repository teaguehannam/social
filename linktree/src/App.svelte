<script>
  import { links } from './Links.js';
</script>

<h1>Teague Hannam</h1>

<main>
  {#each links as i}
    <a href={i.link}>{i.name}</a>
  {/each}
</main>


<style>
  h1 {
    position: fixed;
    bottom: 0;
    right: 0;
    margin: 0;
    line-height: 1.8rem;
    color: rgba(192,192,192,0.15);
    letter-spacing: 0.1vw;
    font-weight: 100;
    font-size: 1.2rem;
    text-align: center;
    padding: 0 2vw;
    background: rgba(0,0,0,0.2);
  }
  main {
    display: grid;
    align-items: center;
  }
  a {
    display: block;
    text-align: center;
    font-size: calc(1.8rem + 1vw);
    line-height: calc(100vh / 5 - (1.8rem  / 5));
    transition: 0.12s all ease-out;
  }
  a:hover, a:active, a:focus {
    backdrop-filter: blur(7px);
    background: rgba(20,20,20,0.6);
    color: white;
  }
</style>
