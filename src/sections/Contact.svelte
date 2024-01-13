<script>
  import githubImage from '/github.webp';
  import linkImage from '/linkedin.webp';
  import TEXTS from '../data/text';
  import URLS from '../data/urls';

  const year = new Date().getFullYear()
</script>

<contact id="contact">
  <section>
    <p>
      {TEXTS?.CONTACT[0]}
    </p>
    <contactContainer>
      <a href={URLS?.GITHUB_PROFILE} target="_blank">
        <img class="gitImg" src={githubImage} title="Raphael Pinto Github" alt="Github" />
      </a>
      <a href={URLS?.LINKED_IN_PROFILE} target="_blank">
        <img src={linkImage} title="Raphael Pinto LinkedIn's profile" alt="LinkedIn">
      </a>
    </contactContainer>
  </section>
  <h2>{TEXTS?.FOOTER[0] + " " + year}</h2>
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

  contactContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5em;
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

  img:hover {
    box-shadow: 5px 5px 10px 0px var(--theme-special-color);
    transition: 0.5s;
  }

  .gitImg {
    border-radius: 50%;
  }
</style>