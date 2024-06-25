<script>
import Navbar from "./lib/Navbar.svelte";

  const apiKey = import.meta.env.VITE_API_KEY;
  console.log("key: " + apiKey);


  let title = "";
  let picData = [{"title":""}];

  async function fetchNASAPic() {
    const response = await fetch(
      "https://api.nasa.gov/planetary/apod?api_key=jGsfUORw1kINP66gGYaU5cvLqrIXTh6NTanfXE8g&count=10",
    );

    const data = await response.json();
    picData = [...data];
    title = picData[0].title;
    console.log("Das ist der Titel " + title);
    console.log(picData);
  }

  fetchNASAPic();

  // async function fetchNASAPic() {
  //       const planetId = params.planetId;

  //       const response = await fetch(
  //           `https://api.le-systeme-solaire.net/rest/bodies/${planetId}`,
  //       );
  //       const data = await response.json();
  //       moons = data.moons;
  //       planetName = data.englishName;
  //   }
</script>

<main>
  <Navbar />
  {#each picData as pic}
  <h1>{pic.title}</h1>
    <img src={pic.url} alt={pic.title} />
  {/each}
  
</main>

<style>
</style>
