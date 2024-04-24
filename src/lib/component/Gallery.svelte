<script lang="ts">
    export let images: { alt: string, src: string }[];
</script>

<div id="gallery">
    {#each images as image}
        <img class="image" alt={image.alt} src={image.src} />
    {/each}
</div>

<style>
    #gallery {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(1, 12vw);
        grid-gap: 15px;
    }
    .image {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
</style>
