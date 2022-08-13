<script>
  import Carousel from "./components/Carousel.svelte";

  let images = [
    {
      title: "london",
      src: "https://images.freeimages.com/images/large-previews/e04/yellow-frontal-with-ivy-1228121.jpg",
    },
    {
      title: "woman sitting",
      src: "https://images.freeimages.com/variants/QFYD44rEJgqdefUFnSMShw7K/f4a36f6589a0e50e702740b15352bc00e4bfaf6f58bd4db850e167794d05993d",
    },
    {
      title: "bike wall",
      src: "https://images.freeimages.com/images/large-previews/70b/bike-red-1423575.jpg",
    },
    {
      title: "green leaves",
      src: "https://images.unsplash.com/photo-1660053586628-3d4b4f56b8a2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHx0b3BpYy1mZWVkfDV8NnNNVmpUTFNrZVF8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60",
    },
    {
      title: "green",
      src: "https://images.unsplash.com/photo-1659993672412-9acc3d19dd68?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHx0b3BpYy1mZWVkfDE1fDZzTVZqVExTa2VRfHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
    },
    {
      title: "waterfall",
      src: "https://images.unsplash.com/photo-1659935275716-69e12c6499e4?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHx0b3BpYy1mZWVkfDIwfDZzTVZqVExTa2VRfHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
    },
  ];

  let title = "🧲 Magnetic Svelte Carousel";
</script>

<svelte:head>
  <title>{title}</title>
</svelte:head>

<h1 class="mx-auto text-5xl  font-bold p-8">{title}</h1>

<section class="flex flex-col items-center">
  <Carousel {images} />
  <slot />
</section>
