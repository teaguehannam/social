<script lang="ts">
</script>

<section>
  {#each new Array(1001) as _, i}
    <main>
      <code>{i}</code>
      <code>🦜</code>
      <code>🐙</code>
      <code>🦕</code>
    </main>
    <main>
      <code>🦕</code>
      <code>{i}</code>
      <code>🦜</code>
      <code>🐙</code>
    </main>
    <main>
      <code>🐙</code>
      <code>🦕</code>
      <code>{i}</code>
      <code>🦜</code>
    </main>
    <main>
      <code>🦜</code>
      <code>🐙</code>
      <code>🦕</code>
      <code>{i}</code>
    </main>
  {/each}
  <main>
    <code>🧉</code>
    <code>🪨</code>
    <code>🛸</code>
  </main>
  <main>
    <code>🛸</code>
    <code>🧉</code>
    <code>🪨</code>
  </main>
</section>

<style>
  section {
    width: 80vw;
    display: grid;
    justify-content: center;
    margin: 12vh auto;
    max-height: 72vh;
    overflow: auto;
    grid-gap: 18px;
    background: rgba(252,252,252,0.1);
    border-radius: 0.3rem;
    backdrop-filter: blur(0.6rem);
    box-shadow: 0 0 24px 3px rgba(30,31,33,1) inset;
  }
  main {
    display: flex;
    justify-content: space-between;
  }
  main:nth-of-type(odd) {
    grid-gap: 2vw;
  }
  code {
    color: rgb(120,120,120);
    line-height: 10vh;
    font-size: calc(1rem + 4vw);
  }
  main:first-of-type,
  main:last-of-type {
    opacity: 0;
  }
</style>
