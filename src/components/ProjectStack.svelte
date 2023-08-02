<script>
  import { onMount } from "svelte";
  export let stack;

  let stacks = [];
  
  onMount(async () => {
    const res = await fetch('/stacks.json')
    stacks = await res.json()
  })
</script>

<stack>
  {#each stack as element}
    <a href={stacks[element]?.url} target="_blank">
      <img src={stacks[element]?.filename} alt={element} title={stacks[element]?.display} />
    </a>
  {/each}
</stack>

<style>
  stack {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    gap: 0.4em;
    flex-wrap: wrap;
    margin-bottom: 2em;
  }

  img {
    object-fit: contain; 
    width: auto; 
    max-height: 50px;
    min-height: 50px; 
    min-width: 50px; 
    background-color: white;
    padding: 2px;
    box-shadow: 5px 5px 10px 0px grey;
  }
</style>