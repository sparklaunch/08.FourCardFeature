<script lang="ts">
    export let data;
</script>

<div class="card">
    <div
        class="card-upperline"
        style="background-color: {data.color.getColorString()}"
    />
    <div class="card-content">
        <h2>{data.title}</h2>
        <p>{data.detail}</p>
        <img src="/assets/{data.icon}" alt={data.title} />
    </div>
</div>

<style>
    .card {
        display: flex;
        flex-direction: column;
        background-color: white;
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 10px 10px 5px rgba(0, 0, 0, 0.1);
        height: 250px;
        max-width: 320px;
    }
    .card-upperline {
        width: 100%;
        height: 5px;
    }
    .card-content {
        padding: 30px;
        display: flex;
        flex-direction: column;
        flex-grow: 1;
    }
    .card-content > h2 {
        color: rgb(80, 80, 100);
        margin-bottom: 10px;
    }
    .card-content > p {
        color: rgb(180, 180, 180);
        flex-grow: 1;
        width: 80%;
    }
    .card-content > img {
        align-self: flex-end;
    }
    @media all and (max-width: 1440px) {
        .card {
            margin: 0;
            margin-bottom: 30px;
            max-width: none;
            align-items: stretch;
        }
    }
</style>
