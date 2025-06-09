<script lang="ts">
    import "../app.css";
    import Foo from "./Foo.svelte";

    let name: string = "giuseppe ErnaNdez";
    let src = "./favicon.png";
    let textFormatted: string =
        "This is a paragraph with <em>some</em> infotext.";
    let count: number = $state(0);

    function increment() {
        count += 1;
    }
</script>

<div class="container mx-auto py-4 mt-30">


    <img {src} alt="Logo" />


    <h1 class="font-bold text-red-400 text-2xl py-7">
        Svelte + tailwindcss
    </h1>

    <h2>hello {name.toUpperCase()}</h2>

    <p class="text-info">This is a paragraph with some infotext.</p>

    <p>{textFormatted}</p>

    <p>{@html textFormatted}</p>

    <button
        onclick={increment}
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
    >
        Count {count}
        {count === 0 ? "Click me!" : "Clicked!"}
    </button>
</div>

<Foo />

<style lang="postcss">
    @reference "tailwindcss";
    .text-info {
        color: black;
        font-size: 1.3rem;
        font-weight: bold;
    }
</style>
