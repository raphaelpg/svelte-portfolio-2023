<script>
  import ProjectItem from "./components/ProjectItem.svelte";
  import SectionTitle from "./components/SectionTitle.svelte";
  import projects from "./data/projects.js";
</script>

<SectionTitle title="Projects" color="--theme-secondary-color" />
<projectsContainer>
  {#each projects as project}
    <ProjectItem 
      img={project?.img}
      title={project?.title}
      description={project?.description}
      stack={project?.stack}
      url={project?.url}
      repo={project?.repo}
      tag={project?.tag}
    />
  {/each}
</projectsContainer>

<style>
  projectsContainer {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    gap: 5em;
  }
</style>