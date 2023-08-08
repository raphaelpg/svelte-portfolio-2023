<script>
  import TEXTS from "../data/text";
  import SectionTitle from "../components/SectionTitle.svelte";

  /* particlesJS.load(@dom-id, @path-json, @callback (optional)); */
  particlesJS.load('particles-js', 'particles.json');
</script>

<home>
  <!-- <div id="particles-js"></div> -->
  <SectionTitle title={TEXTS?.TITLE[0]} color="--theme-secondary-color" />
  <SectionTitle title={TEXTS?.TITLE[1]} color="--theme-primary-color" />
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