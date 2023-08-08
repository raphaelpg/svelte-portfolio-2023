<script>
  import TEXTS from "../data/text";
  import SectionTitle from "../components/SectionTitle.svelte";
</script>

<home>
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