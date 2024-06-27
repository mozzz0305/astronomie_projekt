<script>
    import Cards from "./Cards.svelte";
    import Infos from "./Infos.svelte";
</script>

<main>
    <div class="field">
        <!-- <Cards /> -->
        <Infos />
    </div>
</main>

<style>
    .field {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: calc(100vw - 10%);
        height: calc(100vh - 20%);
        display: flex;
        align-items: center;
        background-color: rgba(77, 77, 77, 0.3);
        backdrop-filter: blur(10px);
        border: 3px solid white;
        border-radius: 100px;
        padding: 100px 100px;
    }
</style>
