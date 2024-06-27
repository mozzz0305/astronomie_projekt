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
        backdrop-filter: blur(30px);
        border: 3px solid white;
        borde