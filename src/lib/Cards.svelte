<script>
    import Card from "./Card.svelte";
    import { apods } from "../store.js";

    function shuffle(array) {
        let currentIndex = array.length, temporaryValue, randomIndex;

        while (0 !== currentIndex) {
            randomIndex = Math.floor(Math.random() * currentIndex);
            currentIndex -= 1;

            temporaryValue = array[currentIndex];
            array[currentIndex] = array[randomIndex];
            array[randomIndex] = temporaryValue;
        }

        return array;
    }

    let shuffledPics = [];

    $: if ($apods.length > 0) {
        const pics = [...$apods, ...$apods];
        shuffledPics = shuffle(pics); 
    }
</script>

<main>
    <div class="wrapper">
        {#if $apods.length === 0}
            <h1>Loading...</h1>
        {/if}
        {#if $apods.length > 0}
            {#each shuffledPics as pic}
                <Card pic={pic.url} title={pic.title} />
            {/each}
        {/if}
    </div>
</main>

<style>
    .wrapper {
        position:absolute;
        width: calc(90vw - 206px);
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
    }
</style>