<script>
  import { onMount } from "svelte";
  import TEXTS from '../data/text.js'

  let scrollPosition = 0;
  const initialNavbarHeight = 15;
  const initialShadow = 0;
  const initialBackground = 'transparent';
  let navbarHeight = initialNavbarHeight;
  let updatedShadow = initialShadow;
  let updatedBackground = initialBackground;

  const handleScroll = () => {
    scrollPosition = window.scrollY;
    navbarHeight = scrollPosition > 0 ? 7 : initialNavbarHeight;
    updatedShadow = scrollPosition > 0 ? 5 : initialShadow;
    updatedBackground = scrollPosition > 0 ? 'white' : initialBackground;
  };

  onMount(() => {
    window.addEventListener("scroll", handleScroll);
    return () => {
      window.removeEventListener("scroll", handleScroll);
    }
  })
</script>

<header style="
  height: {navbarHeight}vh;
  box-shadow: 0 0 {updatedShadow}px grey;
  background-color: {updatedBackground};
">
  <a href="#about">
    <h3>{TEXTS?.NAVBAR[0]}</h3>
  </a>
  <a href="#projects">
    <h3>{TEXTS?.NAVBAR[1]}</h3>
  </a>
  <a href="#about">
    <h3>{TEXTS?.NAVBAR[2]}</h3>
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
    box-shadow: 0 0 5px grey;
  }

  header * {
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: var(--theme-secondary-color);
  }

  h3 {
    text-transform: uppercase;
    font-size: 12px;
  }

  h3:hover {
    color: var(--theme-special-color);
    transition: 0.5s;
  }
</style>