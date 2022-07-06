<script>
  import ocean from './vids/ocean.mp4'
  import loading from './vids/loading.gif'

  // header emojis
  let innerWidth = window.innerWidth || 0;
  let emojis = selectEmojis();
  let textbox;

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

  // music player
  const youtubes = [
    'WIuNAmt15t4',
    'zFfL0y3zyfc',
    'gPAU0v4U0xI',
    'xSh1B70mrnQ',
  ]

  let currentVid = 0;

  const prevYt = () => {
    if (currentVid !== 0) {
      currentVid -= 1;
    } else {
      currentVid = youtubes.length - 1;
    }
  }

  const nextYt = () => {
    if (currentVid + 1 !== youtubes.length) {
      currentVid += 1;
    } else {
      currentVid = 0;
    }
  }

  let intro = '¡Media hosting happens here!'
  function hdlEnter(e) {
    if (e.key === 'Enter') {
      intro = textbox
    }
  }

</script>

<svelte:window bind:innerWidth />

<header on:click={() => emojis = selectEmojis()}>
    <h1>{new String().padStart((innerWidth * 0.04142), emojis)}</h1>
</header>

<section>

  <main>
    <h3>{intro}</h3>
  </main>
  <main>
    <textarea 
      placeholder="free text box"
      bind:value={textbox}
      on:keypress={hdlEnter} />
  </main>

  <main>
    <iframe
      src={`https://www.youtube.com/embed/${youtubes[currentVid]}`}
      title="Song from YouTube"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
    </iframe>
  </main>

  <main>
    <div class="VidControls">
      <code on:click={prevYt}>⏮️</code>
      <h3>{currentVid + 1} / {youtubes.length}</h3>
      <code on:click={nextYt}>⏭️</code>
    </div>
  </main>
  

  <main>
    <video controls>
      <source src={ocean} type="video/mp4">
        - video here -
    </video>
  </main>

  <main>
    <img src={loading} alt="Load vid" />
  </main>

</section>
