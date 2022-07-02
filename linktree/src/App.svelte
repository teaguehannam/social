<script>
  import { Links } from './links.js';
</script>


<div id="Container">
  <main>
    {#each Links as i}
      <a href={i.link}>{i.name}</a>
    {/each}
  </main>
</div>


<style>
  #Container {
    height: 80vh;
    margin: 10vh auto ;
    width:  80vw;
    max-width: 1200px;
    overflow: auto;
  }
  main {
    overflow: auto;
    text-align: center;
    display:  grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    backdrop-filter: blur(12px); /* chromium/safari */
    margin: calc(100vh / 12.5) 0 0 0;
    background: rgba(20,28,28,0.9);
    max-height: calc(100% - 4rem);
    transition: 0.25s box-shadow;
    border-radius: 12px;
    transition-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1);
  }
  main:hover {
    box-shadow:
      rgba(31,193,27,0.2) 0 0 20px 0 inset,
      rgba(31,93,27,0.3) 0px 0px 0px 2px inset;
  }
  a {
    z-index: 20;
    margin: 0;
    cursor:  pointer;
    font-size: 2rem;
    line-height: min(calc(100vh / 7), 128px);
    transition: 0.05s background linear;
    color: rbga(188,189,186,0.8);
  }
  a:hover {
    background: rgba(212,204,206,0.1);
    color: rbga(22,222,22,1);
  }
</style>
