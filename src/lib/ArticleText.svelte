<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 60%;
        background-color: #271c19;
        color: #fffffe;
        padding: 30px;
        font-family: "Manrope", sans-serif;
        font-weight: 500;
        font-size: 18px;
        border-radius: 10px;
        box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;
    }
</style>
