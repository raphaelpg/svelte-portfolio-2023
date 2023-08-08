<script>
  import SectionTitle from "../components/SectionTitle.svelte";
  import githubImage from '/github.webp';
  import linkImage from '/linkedin.webp';
  import profilePicture from'/pro_2023.webp';
  import TEXTS from "../data/text";
</script>

<about id="about">
  <SectionTitle title={TEXTS?.NAVBAR[0]} color="--theme-secondary-color"/>
  <section>
    <img src={profilePicture} alt="Raphael Pinto" />
    <aboutText>
      <p>
        {TEXTS?.ABOUT[0]}
      </p>
      <largeScreen>
        <p>
          {TEXTS?.ABOUT[1]}
        </p>
        <p>
          {TEXTS?.ABOUT[2]}
        </p>
        <links>
          <a href="https://github.com/raphaelpg/" target="_blank">
            <img class="gitImg" src={githubImage} title="Raphael Pinto Github" alt="Github" />
          </a>
          <a href="https://www.linkedin.com/in/raphael-pinto-gregorio-660b2579/" target="_blank">
            <img src={linkImage} title="Raphael Pinto LinkedIn's profile" alt="LinkedIn">
          </a>
        </links>
      </largeScreen>
    </aboutText>
  </section>
  <smallScreen>
    <p>
      {TEXTS?.ABOUT[1]}
    </p>
    <p>
      {TEXTS?.ABOUT[2]}
    </p>
    <links>
      <a href="https://github.com/raphaelpg/" target="_blank">
        <img class="gitImg" src={githubImage} title="Raphael Pinto Github" alt="Github" />
      </a>
      <a href="https://www.linkedin.com/in/raphael-pinto-gregorio-660b2579/" target="_blank">
        <img src={linkImage} title="Raphael Pinto LinkedIn's profile" alt="LinkedIn">
      </a>
    </links>
  </smallScreen>
</about>

<style>
  about {
    display: flex;
    flex-direction: column;
    height: 90vh;
  }

  about img {
    width: auto;
    height: 250px;
  }

  aboutText {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  about p {
    margin: 0;
  }

  largeScreen {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  smallScreen {
    display: none;
  }
  
  section {
    display: flex;
    gap: 1em;
    padding: 6em 0;
  }

  img {
    -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
    filter: grayscale(100%);
    /* box-shadow: 5px 5px 10px 0px grey; */
  }

  links {
    display: flex;
    justify-content: flex-start;
  }

  links img {
    object-fit: contain; 
    width: auto; 
    max-height: 50px;
    min-height: 50px; 
    min-width: 50px; 
    background-color: white;
    padding: 2px;
    -webkit-filter: grayscale(0%); /* Safari 6.0 - 9.0 */
    filter: grayscale(0%);
  }

  links img:hover {
    box-shadow: 5px 5px 10px 0px var(--theme-special-color);
    transition: 0.5s;
  }

  .gitImg {
    border-radius: 50%;
  }

  @media (max-width: 800px) {
    about {
      padding-bottom: 2em;
    }
    
    about img {
      width: auto;
      height: 150px;
    }

    about p {
      margin: 0;
    }

    section {
      display: flex;
      gap: 1em;
      padding: 0;
    }

    largeScreen {
      display: none;
    }

    smallScreen {
      display: flex;
      flex-direction: column;
      gap: 1em;
      margin-top: 1em;
    }

  }
</style>