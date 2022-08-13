<script>
    import { getitemId } from "./Carousel.svelte";

    export let images;

    const scrollIntoView = ({ currentTarget }) => {
        const scrollToElement = document.querySelector(
            currentTarget.getAttribute("href")
        );

        if (!scrollToElement) return;

        const mediaQuery = window.matchMedia("(prefers-reduced-motion: reduce");

        scrollToElement.scrollIntoView({
            behavior: mediaQuery.matches ? "auto" : "smooth",
        });
    };
</script>

<nav>
    <ul>
        {#each images as { title }, index}
            <li>
                <a
                    on:click|preventDefault={scrollIntoView}
                    href={"#" + getitemId(index)}>{title}</a
                >
            </li>
        {/each}
    </ul>
</nav>
