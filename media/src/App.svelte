<script>
  const playlist = new String('https://www.youtube.com/embed?listType=playlist&list=PL5WBz5u6UE9IMTzbFCnCn9EbvVNHxfHWj')
  let innerWidth = new Number(window.innerWidth || 0)
  let emojis = selectEmojis()
  let textbox // html textrea

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
<header on:click={() => emojis = selectEmojis()}>
    <h1 class="NoSelect">
      {new String().padStart((innerWidth * 0.04142), emojis)}
    </h1>
</header>

<iframe src={playlist}
  title="YouTube video"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen
  referrerpolicy="no-referrer-when-downgrade" >
</iframe>
