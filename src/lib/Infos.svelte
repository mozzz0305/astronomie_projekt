<script>
    import Info from "./Info.svelte";
    import { apods } from "../store.js";
</script>

<main>
    <div class = wrapper>
        {#if $apods.length === 0}
        <h1>Loading...</h1>
    {/if}
    {#if $apods.length > 0}
        {#each $apods as pic}
            <Info
                pic={pic.url}
                title={pic.title}
                date={pic.date}
                explanation={pic.explanation}
            />
        {/each}
    {/if}
    </div>
</main>

<style>
    .wrapper{
        position:absolute;
        width: calc(90vw - 206px)
    }
</style>