<script>
    export let id;
    export let src;
    export let title;
</script>

<li {id} class="shrink-0 snap-center shadow-lg relative">
    <img class="rounded h-96 w-64 object-cover" {src} {title} alt={title} />
    <button
        class="bg-blue-600 text-white px-4 py-2 font-semibold rounded absolute inset-x-2 bottom-2"
        >{title}</button
    >
</li>
