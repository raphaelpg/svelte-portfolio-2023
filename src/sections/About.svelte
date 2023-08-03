<script>
  import SectionTitle from "../components/SectionTitle.svelte";
  let src = '/pro_2023.webp';
</script>

<about id="about">
  <SectionTitle title="About" color="--theme-secondary-color"/>
  <section>
    <img {src} alt="Raphael Pinto" />
    <aboutText>
      <p>
        I embarked on a journey to learn web development initially creating websites for friends as a freelancer. 
        As my skills evolved, I seized the opportunity to explore the exciting world of blockchain technology by attending a specialized course and participating in web3 hackathons, collaborating with talented individuals from diverse backgrounds.
      </p>
      <p>
        Today, I continue to pursue my passion for web development and I believe in delivering high-quality solutions, prioritizing the user experience above all.
        As a team player, I thrive in collaborative environments and prioritize building trust among my peers.
      </p>
      <p>
        When I'm not immersed in coding, you can find me riding my motorbike, exploring new video games, indulging in movies, or escaping into the realms of science fiction literature.
      </p>
    </aboutText>
  </section>
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
</style>