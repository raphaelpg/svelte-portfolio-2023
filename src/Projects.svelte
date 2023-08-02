<script>
  import ProjectItem from "./components/ProjectItem.svelte";
  import SectionTitle from "./components/SectionTitle.svelte";
</script>

<SectionTitle title="Projects" color="--theme-secondary-color" />
<projectsContainer>
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
  <ProjectItem 
    img="/portfolio23.webp"
    title="Portfolio 2023"
    description="New version of my personnal portoflio, the main objective was to learn Next JS and Tailwind. Solo project."
    stack={[
      'nextjs',
      'tailwind',
      'react',
      'typescript',
      'copilot',
    ]}
    url="https://raphaelpg.github.io/nextjs-portfolio-2023/"
    repo="https://github.com/raphaelpg/nextjs-portfolio-2023"
  />
</projectsContainer>

<style>
  projectsContainer {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    gap: 5em;
  }
</style>