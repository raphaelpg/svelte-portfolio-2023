<script>
  import { onMount } from "svelte";

  let scrollPosition = 0;
  const initialNavbarHeight = 15;
  let navbarHeight = initialNavbarHeight;

  const handleScroll = () => {
    scrollPosition = window.scrollY;
    navbarHeight = scrollPosition > 0 ? 7 : initialNavbarHeight;
  };

  onMount(() => {
    window.addEventListener("scroll", handleScroll);
    return () => {
      window.removeEventListener("scroll", handleScroll);
    }
  })
</script>

<header style="height: {navbarHeight}vh;">
  <a href="#about">
    <h3>About</h3>
  </a>
  <a href="#projects">
    <h3>Projects</h3>
  </a>
  <a href="#contact">
    <h3>Contact</h3>
  </a>
</header> 

<style>
  header {
    z-index: 1;
    position: fixed;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    width: 100%;
    transition: height 0.2s ease-in-out;
    background-color: white;
    box-shadow: 0 0 5px grey;
  }

  header * {
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: var(--theme-secondary-color);
  }
</style>