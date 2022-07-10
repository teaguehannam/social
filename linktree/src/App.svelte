<script>
  const Links = [
    {
      "name": "Github",
      "link": "https://github.com/teaguehannam"
    },
    {
      "name": "Media",
      "link": "https://media.teaguehannam.com/"
    },
    {
      "name": "Notes",
      "link": "https://notes.teaguehannam.com/"
    },
    {
      "name": "Nutrients",
      "link": "https://currentnutrients.com/"
    },
    {
      "name": "YouTube",
      "link": "https://www.youtube.com/channel/UCZOwiWmYnooVVsVAYmewOhg/playlists"
    },
  ]
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
