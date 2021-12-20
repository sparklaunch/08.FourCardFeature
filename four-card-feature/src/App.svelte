<script lang="ts">
    import Title from "./components/Title.svelte";
    import Section from "./components/Section.svelte";
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
        href="https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;600&display=swap"
        rel="stylesheet"
    />
</svelte:head>
<div id="app">
    <Title />
    <Section />
</div>

<style>
    #app {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
