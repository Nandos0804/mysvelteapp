<script lang="ts">
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

<h1>hello {name.toUpperCase()}</h1>

<img {src} alt="Logo" />

<p class="text-info">This is a paragraph with some infotext.</p>

<p>{textFormatted}</p>

<p>{@html textFormatted}</p>

<button onclick={increment}>
    Count {count}
    {count === 0 ? "Click me!" : "Clicked!"}
</button>

<Foo />

<style>
    .text-info {
        color: red;
        font-size: 2rem;
        font-weight: bold;
    }
</style>
