<script>
    let { title, subtitle } = $props();
</script>

<div class="title-card">
    <div class="content">
        <h1>{title}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-color: #55423d;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
    }

    .content {
        max-width: 900px;
        background-color: #271c19;
        padding: 2rem;
        border-radius: 5px;
        box-shadow: rgb(150, 86, 161) 0px 0px 0px 6px, rgb(231, 143, 179) 0px 0px 0px 12px;
    }

    h1 {
        font-size: 3rem;
        margin: 0;
        color: #ffc0ad;
        font-size: 45px;
        font-family: "Winky Rough", sans-serif;
    }

    p {
        font-size: 1.3rem;
        color: #fffffe;
        margin-top: 1rem;
        font-family: "Manrope", sans-serif;
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.2rem;
        }

        p {
            font-size: 1.1rem;
        }
    }
</style>
