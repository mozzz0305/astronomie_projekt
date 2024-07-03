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

    @media (max-width: 900px) {
        h1 {
            font-size: 20px;
        }
    }

    @media (max-width: 600px) {
        .infobox {
            grid-template-columns: 1fr;
            grid-template-rows: 100px 35px 20px 180px;
            max-height: 300px;
        }

        img {
            grid-column: 1 / 2;
            grid-row: 1 / 2;
            width: 50%;
            height: 100%;
            object-fit: cover;
            border-radius: 2px;
            padding-bottom: 10px;
        }

        h1 {
            grid-column: 1 / 2;
            grid-row: 2/3;
            font-size: 20px;
            padding-left: 0px;
        }

        h6 {
            grid-column: 1 / 2;
            grid-row: 3/4;
            font-size: 12px;
            margin-right: 0px;
            text-align: left;
            padding-bottom: 10px;
        }

        p {
            grid-column: 1 / 2;
            grid-row: 4/5;
            font-size: 10px;
            padding-left: 0px;
        }
    }
</style>
