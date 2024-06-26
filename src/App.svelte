<script>
  import Navbar from "./lib/Navbar.svelte";
  import Field from "./lib/Field.svelte";
  import Card from "./lib/Card.svelte";
  import { apods } from "./store.js";

  const apiKey = import.meta.env.VITE_API_KEY;
  console.log("key: " + apiKey);

  async function fetchNASAPic() {
    const response = await fetch(
      "https://api.nasa.gov/planetary/apod?api_key=jGsfUORw1kINP66gGYaU5cvLqrIXTh6NTanfXE8g&count=10",
    );

    const data = await response.json();
    $apods = [...data];
  }

  fetchNASAPic();
</script>

<main>
  <Navbar />
  <Field />
  {#if $apods.length === 0}
    <h1>Loading...</h1>
  {/if}
  {#if $apods.length > 0}
    <Card pic={$apods[0].url} picTitle={$apods[0].title} />
    {#each $apods as pic}
      <h1>{pic.title}</h1>
      <img src={pic.url} alt={pic.title} />
    {/each}
  {/if}
</main>

<style>
</style>
