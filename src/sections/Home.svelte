<script>
  import SectionTitle from "../components/SectionTitle.svelte";
</script>

<home>
  <SectionTitle title="Raphael Pinto" color="--theme-secondary-color" />
  <SectionTitle title="Fullstack Developer" color="--theme-primary-color" />
</home>

<style>
  home {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100vh;
    transform: translateY(-15vh);
  }
</style>