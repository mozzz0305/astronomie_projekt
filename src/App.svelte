<script>
  import Router from "svelte-spa-router";
  import Navbar from "./lib/Navbar.svelte";
  import Field from "./lib/Field.svelte";
  import Score from "./lib/Score.svelte";
  import { apods } from "./store.js";
    import Cards from "./lib/Cards.svelte";
    import Info from "./lib/Info.svelte";

  const apiKey = import.meta.env.VITE_API_KEY;

  async function fetchNASAPic() {
    const response = await fetch(
      "https://api.nasa.gov/planetary/apod?api_key=jGsfUORw1kINP66gGYaU5cvLqrIXTh6NTanfXE8g&count=12&thumbs=true",
    );

    const data = await response.json();
    $apods = [...data];
  }

  fetchNASAPic();

  const routes = {
        "/Game": Score,
    };
</script>

<main>
  <img src="/Star.svg" alt="Star" class="star1">
  <img src="/Star.svg" alt="Star" class="star2">
  <img src="/Star.svg" alt="Star" class="star3">
  <img src="/Star.svg" alt="Star" class="star4">
  <Field />
  <Navbar />
  <!-- <Score /> -->
  <Router {routes} />
</main>

<style>
  img {
    position: fixed;
  }
  .star1{
    scale: 1;
    top: 10%;
    left: 10%;
  }
  .star2{
    scale: 0.5;
    top: 10%;
    left: 80%;
  }
  .star3{
    scale: 0.5;
    top: 80%;
    left: 10%;
  }
  .star4{
    scale: 0.55;
    top: 80%;
    left: 80%;
  }
</style>
