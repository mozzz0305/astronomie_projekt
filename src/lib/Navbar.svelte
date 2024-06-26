<!-- Wie zeigt man an ob "Game" oder "Info" ausgewählt ist? -->

<script>
    // Script-Inhalt, falls benötigt
</script>

<main>
    <nav>
        <h1>MEMORY</h1>
        
        <ul>
            <li>
                <a href="#">Game</a>
            </li>
            <li>
                <a href="#">Info</a>
            </li>
        </ul>
        <!-- <div>Game</div>
        <div class="info-button">Info</div> -->
    </nav>
</main>

<style>
    nav {
        position: fixed;
        top: 85%;
        left: 50%;
        transform: translateX(-50%);
        width: 600px;
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        background-color: rgba(139, 139, 139, 0.3);
        backdrop-filter: blur(30px);
        border: 3px solid white;
        border-radius: 50px;
        padding: 10px 40px;
    }

    h1 {
        margin: 0;
        color: white;
        font-size: 40px;
        font-weight: bold;
    }

    ul {
        display: flex;
        justify-content: space-around;
        list-style-type: none;
    }

    a {
        color: white;
        margin: 0 10px;
        text-decoration: none;
        font-size: 30px;
    }

    .info-button {
        background-color: white;
        color: black;
        border-radius: 50%;
        width: 30px;
        height: 30px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
