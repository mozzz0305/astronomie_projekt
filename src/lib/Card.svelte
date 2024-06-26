<script>
    export let pic;
    export let picTitle;

    // Variable to track the opacity state
    let isOpaque = false;

    // Function to toggle opacity
    function toggleOpacity() {
        isOpaque = !isOpaque;
    }
</script>

<main>
    <div class="card">
        <img src="{pic}" alt="{picTitle}" on:click="{toggleOpacity}" class:opaque={isOpaque}>
    </div>
</main>

<style>
    .card {
        width: 120px;
        height: 120px;
        background-color: #B664C4;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 5px;
        box-sizing: border-box;
    }

    img {
        width: 100%;
        height: 100%;
        border-radius: 2px;
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    .opaque {
        opacity: 1;
    }
</style>