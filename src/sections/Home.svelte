<script>
  import TEXTS from "../data/text";
  import HomeTitle from "../components/HomeTitle.svelte";

  /* particlesJS.load(@dom-id, @path-json, @callback (optional)); */
  particlesJS.load('particles-js', 'particles.json');
</script>

<home>
  <HomeTitle title={TEXTS?.TITLE[0]} color="--theme-secondary-color" />
  <HomeTitle title={TEXTS?.TITLE[1]} color="--theme-primary-color" />
</home>

<style>
  home {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100vh;
  }
</style>