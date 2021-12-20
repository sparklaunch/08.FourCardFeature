<script lang="ts">
    import Card from "./Card.svelte";
    export let data;
</script>

<div id="section">
    <Card data={data[0]} />
</div>
