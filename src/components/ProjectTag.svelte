<script>
  export let tag;

  const backgroundColors = {
    "Personal Project": {color: "--theme-tag-blue"},
    "Professional Project": {color: "--theme-tag-green"},
    "Hackathon Project": {color: "--theme-tag-yellow"}
  }

  let tagColor = `var(${backgroundColors[tag]?.color})` ?? 'white'
</script>

<p style="background-color: {tagColor}">{tag}</p>

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
</style>