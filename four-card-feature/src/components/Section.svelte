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
</style>
