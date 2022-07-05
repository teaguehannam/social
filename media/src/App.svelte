<script>
  import ocean from './vids/ocean.mp4'
  import loading from './vids/loading.gif'
  import test from './audio/test.mp3'


  // header emojis
  let innerWidth = window.innerWidth || 0;
  let possibleEmojis = ['🤖','🦆','🌵'];
  let emojis = selectEmojis();

  function selectEmojis() {
    let randomize = possibleEmojis.sort(() => 0.5 - Math.random());
    randomize.unshift('🧙‍♂️')
    return randomize.slice(0, 4)
  }

</script>

<svelte:window bind:innerWidth />

<header>
    <h1>{new String().padStart((innerWidth * 0.043), emojis)}</h1>
</header>

<section>

  <h3>Media hosting happens here!</h3>


  <iframe src="https://notes.teaguehannam.com/"></iframe>


  <code>video</code>
  <main>
    <video controls>
      <source src={ocean} type="video/mp4">
        - video here -
    </video>
  </main>

  <code>audio</code>
  <main>
    <audio controls>
      <source src={test} type="audio/mp3">
        - audio here -
    </audio>
  </main>

  <code>image</code>
  <main>
    <img src={loading} alt="Load vid" />
  </main>

</section>


<style>
  header {
    position: sticky;
    top: 0;
    backdrop-filter: blur(9px);
    background: rgba(240,240,240,0.3);
    z-index: 5;
  }
  header > h1 {
    color: rgba(0,0,0,0.6);
    text-align: center;
    letter-spacing: 0.4vw;
    line-height: 3rem;
  }
  section {
    display: grid;
    padding: 10vh 0;
    grid-gap: 5vh;
    width: 90%;
    max-width: 900px;
    margin: 0 auto;
  }
  main, main > video, main > img {
    margin: 0 auto;
    max-height: 40vh;
  }
  img {
    border-radius: 50%;
  }
  code {
    text-align: center;
    font-size: 2rem;
    color: rgba(15,225,10,0.9);
  }
  iframe {
    border: 2px solid rgba(50,51,53,0.6);
    backdrop-filter: blur(3px);
    width: 100%;
  }
  iframe:hover, iframe:focus {
    opacity: 1;
  }

</style>
