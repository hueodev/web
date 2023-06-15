<script>
    import RichPresence from "./RichPresence.svelte";
</script>

<main>
    <div class="container">
        <img src="/img.png" alt="">
        <div class="info">
            <h1>Hugo</h1>
            <p>Student Web developer</p>
            <RichPresence/>
        </div>
    </div>
</main>

<style lang="scss">
    .container {
        display: flex;
        gap: 2rem;
        margin: auto;
        max-width: 28rem;
    }

    img {
        margin: auto 0;
        width: 100px;
        height: 100px;
        border-radius: 100%;
    }

    .info {
        margin: auto 0;
    }

    h1 {
        font-size: 1.3rem;
        font-weight: 600;
    } 

    p {
        font-size: 1.3;
        color: rgb(163, 163, 163);
        margin: .2rem 0;
    }
</style>