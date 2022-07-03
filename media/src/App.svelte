<script>
  import ocean from './vids/ocean.mp4'
  import loading from './vids/loading.gif'
  import test from './test.mp3';

  const cWidth = window.innerWidth;
</script>

<header>Welcome to free media</header>

<main>
  <code>Video</code>
  <video controls>
    <source src={ocean} type="video/mp4">
      - video here -
  </video>
  <code>Gif</code>
  <img src={loading} alt="Load vid" />
  <code>iframe</code>
  <iframe src="https://2nami.com/"></iframe>
</main>

<style>
  header {
    background: rgba(252,252,252,0.2);
    text-indent: 0.4rem;
  }
  main {
    max-width: 900px;
    margin: 5vh auto 20vh auto;
    grid-gap: 1.2rem;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
  }
  video, img {
    max-width: 720px;
  }
  iframe {
    width: 90vw;
    max-width: 900px;
    height: 50vh;
  }
  code {
    color: green;
  }
  code:nth-of-type(2) {
    text-align: center;
  }
  code:nth-of-type(3) {
    text-align: right;
  }
</style>
