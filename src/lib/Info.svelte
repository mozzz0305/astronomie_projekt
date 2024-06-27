<script>
    export let pic;
    export let title;
    export let date;
    export let explanation;
</script>

<main>
    <div class="infobox">
        <img
            src="{pic}"
            alt="{title}"
        />
        <h1>{title}</h1>
        <h6>{date}</h6>
        <p>
            {explanation}
        </p>
    </div>
</main>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .infobox {
        max-height: 160px;
        display: grid;
        grid-template-columns: 160px auto 1fr;
        grid-template-rows: 35px 120px;
        overflow: hidden;
        margin: 50px 0px;
    }

    img {
        grid-column: 1 / 2;
        grid-row: 1 / 3;
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 2px;
    }

    h1 {
        grid-column: 2 / 3;
        grid-row: 1 / 2;
        font-size: 25px;
        font-weight: bold;
        padding: 0px;
        color: white;
        padding-left: 25px;
    }

    h6 {
        grid-column: 3 / 4;
        grid-row: 1 / 2;
        font-size: 15px;
        font-weight: bold;
        color: #cccccc;
        text-align: right;
        align-self: center;
        margin-right: 20px;
    }

    p {
        grid-column: 2 / 4;
        grid-row: 2 / 3;
        font-size: 13px;
        color: white;
        padding-left: 25px;
    }
</style>
