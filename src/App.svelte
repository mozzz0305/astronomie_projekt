<script>
  import Navbar from "./lib/Navbar.svelte";
  import Card from "./lib/Card.svelte";

  let bspPic = "assets/bspPic.jpg";

  const apiKey = import.meta.env.VITE_API_KEY;
  console.log("key: " + apiKey);

  let title = "";
  let picData = [{ title: "" }];

  async function fetchNASAPic() {
    const response = await fetch(
      "https://api.nasa.gov/planetary/apod?api_key=jGsfUORw1kINP66gGYaU5cvLqrIXTh6NTanfXE8g&count=10",
    );

    const data = await response.json();
    picData = [...data];
    // title = picData[0].title;
    // console.log("Das ist der Titel " + title);
    console.log(picData);
  }

  fetchNASAPic();
</script>

<main>
  <Navbar />
  <Card pic={picData[0].url} picTitle={picData[0].title}/>
  {#each picData as pic}
    <h1>{pic.title}</h1>
    <img src={pic.url} alt={pic.title} />
  {/each}
</main>

<style>
</style>
