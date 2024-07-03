<script>
    export let pic;
    export let title;

    let isOpaque = false;

    function toggleOpacity() {
        isOpaque = !isOpaque;
    }
</script>

<main>
    <div class="card">
        <img src={pic} alt={title} on:click={toggleOpacity} class:opaque={isOpaque}/>
    </div>
</main>

<style>
    .card {
        width: 120px;
        height: 120px;
        background-color: #b664c4;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        box-sizing: border-box;
        border: 2px solid #DADADA;
    }
    
    .card:hover {
        cursor: pointer;
        scale: 1.03;
        transition: scale 0.1s ease;
    }

    img {
        width: 100%;
        height: 100%;
        border-radius: 2px;
        opacity: 0;
        transition: opacity 0.3s ease;
        object-fit: cover;
    }

    .opaque {
        opacity: 1;
    }
</style>