<script>
  import ProjectStack from "./ProjectStack.svelte";

  export let img;
  export let title;
  export let description;
  export let url;
  export let repo;
  export let stack;
</script>

<projectItem>
  <img src={img} alt={title} {title} />
  <projectItemRight>
    <h2>{title}</h2>
    <p>{description}</p>
    <h4>Stack:</h4>
    <ProjectStack {stack} />
    {#if url && url.length > 1}
      <a href={url} target="_blank">View &#10148;</a>
    {/if}
    {#if repo && repo.length > 1}
      <a href={repo} target="_blank">Github &#10148;</a>
    {/if}
  </projectItemRight>
</projectItem>

<style>
  projectItem {
    display: flex;
    justify-content: flex-start;
    align-items: start;
    gap: 1em;
  }

  h2 {
    margin: 0;
  }

  h4 {
    margin-bottom: 0;
  }

  img {
    color: transparent;
    object-fit: contain;
    width: auto;
    min-height: 50px;
    max-width: 250px;
    min-width: 250px;
    background-color: white;
    padding: 2px;
    box-shadow: 5px 5px 10px 0px grey;
  } 

  projectItemRight {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }

  p {
    margin-bottom: 0;
  }

  a {
    text-decoration: none;
    color: inherit;
    font-weight: 600;
  }
</style>

