<script context="module">
    export const getitemId = (index, name = "carousel") =>
        `${name}-item-${index}`;
</script>

<script>
    import ReviewCard from "./ReviewCard.svelte";

    export let images;
</script>

<ul
    class="flex overflow-x-auto gap-6 snap-x snap-mandatory before:shrink-0 before:w-[33vw] after:shrink-0 after:w-[33vw] pb-6"
>
    {#each images as { title, src }, index}
        <ReviewCard id={getitemId(index)} {title} {src} />
    {/each}
</ul>
