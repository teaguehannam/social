<script>
  import ocean from './vids/ocean.mp4'
  import loading from './vids/loading.gif'
  import test from './audio/test.mp3'

  // header emojis
  let innerWidth = window.innerWidth || 0;
  let emojis = selectEmojis();

  function selectEmojis() {
    let randomize = [
      '🤖','🦆','🌵',
      '🤔','🤤','😷',
      '😎','👻','👽',
      '👇','🤘','✌',
      '😹','💀','💦'].sort(() => 0.5 - Math.random());

    randomize.unshift('🧙‍♂️'); // always have wizard
    return new String(randomize.slice(0, 3)).replace(/,/g, '');
  }

</script>

<svelte:window bind:innerWidth />

<header>
    <h1>{new String().padStart((innerWidth * 0.0429), emojis)}</h1>
</header>

<section>

  <main>
    <h3>¡Media hosting happens here!</h3>
  </main>
  
  <main>
    <textarea placeholder="enter text here" />
  </main>

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
