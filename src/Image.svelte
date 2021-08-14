<script>
    export let url;
    export let position
</script>

<div class="image-container" style="background-image: url('{url}'); background-size: cover; background-position: {position};">
</div>

<style>
    .image-container {
        height: 100vh;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        user-select: none;
    }
</style>