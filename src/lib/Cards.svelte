<script>
    import Card from "./Card.svelte";
    import { apods } from "../store.js";
</script>

<main>
    <div class="wrapper">
        {#if $apods.length === 0}
            <h1>Loading...</h1>
        {/if}
        {#if $apods.length > 0}
            {#each $apods as pic}
                <Card pic={pic.url} title={pic.title} />
            {/each}
            {#each $apods as pic}
                <Card pic={pic.url} title={pic.title} />
            {/each}
        {/if}
    </div>
</main>

<style>
    .wrapper {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
    }
</style>
