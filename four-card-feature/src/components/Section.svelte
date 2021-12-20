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
