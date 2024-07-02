<script>
        let scoreP1 = 0;
        let scoreP2 = 0;
</script>

<main>
    <div class="scoreboard">
        <p>{scoreP1} : {scoreP2}</p>
    </div>
</main>

<style>
    .scoreboard {
        position: fixed;
        top: calc(10% - 50px);
        left: 50%;
        transform: translateX(-50%);
        width: 400px;
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgba(77, 77, 77, 0.3);
        -webkit-backdrop-filter: blur(30px);
        backdrop-filter: blur(30px);
        border: 3px solid white;
        border-radius: 50px;
        padding: 10px 40px;
    }

    p {
        font-size: 60px;
        font-weight: bold;
        color: white;
    }
</style>
