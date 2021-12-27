<script lang="ts">
    import Card from "./Card.svelte";
    export let data;
</script>

<div id="section">
    <div id="left">
        <Card data={data[0]} />
    </div>
    <div id="center">
        <Card data={data[1]} />
        <Card data={data[2]} />
    </div>
    <div id="right">
        <Card data={data[3]} />
    </div>
</div>

<style>
    #section {
        display: flex;
        align-items: center;
    }
    #left {
        margin-right: 30px;
    }
    #center {
        margin-right: 30px;
        display: grid;
        row-gap: 30px;
    }
    @media all and (max-width: 1440px) {
        #section {
            flex-direction: column;
            align-items: stretch;
            width: 90%;
        }
        #left {
            margin-right: 0;
        }
        #center {
            margin-right: 0;
            display: flex;
            flex-direction: column;
            align-items: stretch;
            row-gap: 0;
        }
    }
</style>
