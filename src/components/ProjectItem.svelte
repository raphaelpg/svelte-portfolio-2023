<script>
  import ProjectStack from "./ProjectStack.svelte";
  import ProjectTag from "./ProjectTag.svelte";

  export let img;
  export let title;
  export let description;
  export let url;
  export let repo;
  export let stack;
  export let tag;
</script>

<projectItem>
  <img src={img} alt={title} {title} />
  <projectItemRight>
    <h2>{title}</h2>

    {#each description as phrase}
      <p>{phrase}</p>
    {/each}
    
    <h3>Stack:</h3>
    <ProjectStack {stack} />
    
    {#if url && url.length > 1}
      <a href={url} target="_blank">View &#10148;</a>
    {/if}
    {#if repo && repo.length > 1}
      <a href={repo} target="_blank">Github &#10148;</a>
    {/if}
  </projectItemRight>
  <ProjectTag {tag} />
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

  h3 {
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
    margin: 0;
  }

  a {
    text-decoration: none;
    color: var(--theme-secondary-color);
    font-weight: 600;
  }
  
  a:hover {
    color: var(--theme-special-color);
    transition: 0.5s;
  }

  @media (max-width: 800px) {
    projectItem {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: start;
      gap: 1em;
    }

    img {
      color: transparent;
      object-fit: contain;
      width: auto;
      min-height: 50px;
      max-width: 100%;
      min-width: 250px;
      background-color: white;
      padding: 2px;
      box-shadow: 5px 5px 10px 0px grey;
    } 
  }
</style>

