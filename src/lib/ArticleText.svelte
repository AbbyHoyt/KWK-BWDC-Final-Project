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
        /*border: solid #e78fb3 3px;*/
        padding: 30px;
        font-family: "Manrope", sans-serif;
        font-weight: 500;
        font-size: 18px;
        /*box-shadow: rgb(150, 86, 161) 0px 0px 0px 6px, rgb(231, 143, 179) 0px 0px 0px 12px;*/
        border-radius: 10px;
        /*box-shadow: 16px 16px #8aa6df;*/
        /*box-shadow: 6px 6px #dbdbdb;*/
        box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;
    }
</style>
