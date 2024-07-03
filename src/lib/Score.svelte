<script>
    let scoreP1 = 0, scoreP2 = 0;

    function incrementScoreP1() {
        scoreP1 += 1;
    }

    function incrementScoreP2() {
        scoreP2 += 1;
    }
</script>

<main>
    <div class="scoreboard">
        <div class = button on:click={(incrementScoreP1)}>
            <t>+</t>
        </div>
        <p>{scoreP1} : {scoreP2}</p>
        <div class = button on:click={(incrementScoreP2)}>
            <t>+</t>
        </div>
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
        justify-content: space-between;
        background-color: rgba(77, 77, 77, 0.3);
        -webkit-backdrop-filter: blur(30px);
        backdrop-filter: blur(30px);
        border: 3px solid white;
        border-radius: 50px;
        padding: 10px 40px;
    }

    .button {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        background-color: rgb(77, 77, 77);
        border-radius: 50%;
        font-size: 30px;
        font-weight: bold;
        color:grey
    }

    .button:hover {
        background-color: rgb(140, 140, 140);
        color: white;
        cursor: pointer;
    }

    p {
        font-size: 60px;
        font-weight: bold;
        color: white;
    }
</style>
