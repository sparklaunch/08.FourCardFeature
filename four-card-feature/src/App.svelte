<script lang="ts">
    import Title from "./components/Title.svelte";
    import Section from "./components/Section.svelte";
    class Color {
        r: number;
        g: number;
        b: number;
        a: number;
        constructor(r: number, g: number, b: number, a: number = 1) {
            this.r = r;
            this.g = g;
            this.b = b;
            this.a = a;
        }
        getColorString(): string {
            return `rgba(${this.r}, ${this.g}, ${this.b}, ${this.a})`;
        }
    }
    interface Data {
        title: string;
        detail: string;
        icon: string;
        color: Color;
    }
    const data: Data[] = [
        {
            title: "Supervisor",
            detail: "Monitors activity to identify project roadblocks",
            icon: "icon-supervisor.svg",
            color: new Color(110, 210, 210),
        },
    ];
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
    <Section {data} />
</div>

<style>
    #app {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
