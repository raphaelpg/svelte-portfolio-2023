<script>
  export let tag;

  const backgroundColors = {
    "Personal Project": {background: "--theme-tag-blue", color: "white"},
    "Professional Project": {background: "--theme-tag-green", color: "--theme-tag-black"},
    "Hackathon Project": {background: "--theme-tag-yellow", color: "--theme-tag-black"}
  }

  let tagBackground = `var(${backgroundColors[tag]?.background})` ?? 'white'
  let tagColor = `var(${backgroundColors[tag]?.color})` ?? 'white'
</script>

<p style="
  background-color: {tagBackground};
  color: {tagColor};
  ">
  {tag}
</p>

<style>
  p {
    position: absolute;
    right: 13%;
    rotate: 45deg;
    transform: translateY(-20px) translateX(10px);
    width: 100px;
    text-align: center;
    color: white;
    border-radius: 5px;
    padding: 1px 5px;
    font-size: small;
    font-weight: 600;
    letter-spacing: 1px;
    box-shadow: 5px 5px 5px 0px grey;
  }

  @media (max-width: 800px) {
    p {
      position: absolute;
      right: 4%;
      rotate: 45deg;
      transform: translateY(-20px) translateX(10px);
      width: 100px;
      text-align: center;
      color: white;
      border-radius: 5px;
      padding: 1px 5px;
      font-size: small;
      font-weight: 600;
      letter-spacing: 1px;
      box-shadow: 5px 5px 5px 0px grey;
    }
  }
</style>