<script>
    let number = $state([1]);
    import "../app.css";

    function addNumber() {
        // versione a
        number[number.length] = number.length + 1;
        // versione b
        // number.push(number.length + 1);
    }
</script>

<div class="container mx-auto py-10">
    <h2 class="text-3xl font-bold underline">test</h2>
    <p class="py-3">container foo</p>
    <p class="py-3">questi p non ereditano da parent component</p>
</div>

<div class="container mx-auto">
    <button onclick={addNumber} class="btn">
        <h3>{number[number.length - 1]}</h3>
    </button>
</div>

<style lang="postcss">
    @reference "tailwindcss";
    :global(html) {
        background-color: theme(--color-gray-100);
    }
    .btn {
        @apply bg-blue-500 text-white font-bold py-2 px-4 rounded;
    }
</style>
