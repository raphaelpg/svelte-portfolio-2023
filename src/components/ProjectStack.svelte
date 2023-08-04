<script>
  import stacks from '../data/stacks.js';
  export let stack;
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
    height: 50px;
    width: auto; 
    max-height: 50px;
    min-height: 50px; 
    min-width: 50px; 
    background-color: white;
    padding: 2px;
    box-shadow: 5px 5px 10px 0px grey;
  }
</style>