<script>
  import Header from "./sections/Header.svelte";
  import Home from "./sections/Home.svelte";
  import Contact from "./sections/Contact.svelte";
  import Projects from "./sections/Projects.svelte";
  import About from "./sections/About.svelte";
</script>

<Header />
<div id="particles-js" style='
  width: 100%;  
  height: auto;
  position: absolute;
'></div>
<main>
  <Home />
  <About />
  <Projects />
  <Contact />
</main>

<style>
  @media (max-width: 800px) {
    div {
      display: none;
    }
  }

</style>