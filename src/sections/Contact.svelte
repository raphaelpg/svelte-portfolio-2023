<script>
  import githubImage from '/github.webp';
  import linkImage from '/linkedin.webp';

  const year = new Date().getFullYear()
</script>

<contact id="contact">
  <section>
    <h3>Contact Me:</h3>
    <a href="https://github.com/raphaelpg/" target="_blank">
      <img src={githubImage} title="Raphael Pinto Github" alt="Github" />
    </a>
    <a href="https://www.linkedin.com/in/raphael-pinto-gregorio-660b2579/" target="_blank">
      <img src={linkImage} title="Raphael Pinto LinkedIn's profile" alt="LinkedIn">
    </a>
  </section>
  <h2>Raphael Pinto {year}</h2>
</contact>

<style>
  contact {
    height: 92vh;
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: center;
    gap: 10em;
    padding: 0px 0 10vh 0;
  }

  img {
    object-fit: contain; 
    width: auto; 
    max-height: 50px;
    min-height: 50px; 
    min-width: 50px; 
    background-color: white;
    padding: 2px;
  }
</style>