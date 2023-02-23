<script>
    import data from "../data.json";
</script>

<div class="container">
    <div class="text">
        <h1>Get in Touch</h1>
        <p>If you'd like to collab on a small project or just want to say hello, feel free to send me an email. You can also contact me on discord Ogooo#7072</p>
    </div>
    <div class="tags">
        {#each data.links as link}
            <p><a href={link.url} target="_blank" rel="noopener noreferrer">{link.name}</a></p>
        {/each}
    </div>
</div>

<style lang="scss">
.container {
    position: relative;
    margin: auto;
    padding: 3rem 2rem 2rem 2rem;
    max-width: 45rem;  
}

.text {
    text-align: left;
    text-decoration: none;
    h1 {
        margin-bottom: 0.4rem;
        color: rgb(255, 255, 255);
    }
    p {
        font-size: 20px;
        margin-bottom: 0.6rem;
        color: rgb(212, 212, 216);
    }
}

.tags {
    display: grid;
    gap: 1rem;
    grid-template-columns: 1fr 1fr;
    margin: 1rem 0rem 1rem 0rem;
    p {
        max-width: 40rem;
        padding: .4rem 0rem;
        text-align: center;
        font-size: 20px;
        border-radius: .6rem;
        background: #1d1d20;
        border-radius: 6px;
        border: 2px solid rgb(33, 33, 37);
        transition: 400ms ease-in-out;
        &:hover {
            border: 2px solid rgb(42, 77, 136);
            transform: scale(1.02);
        }
    }
    a {
        text-decoration: none;
        color: rgb(255, 255, 255);
    }
}

@media (max-width: 668px) {
    .tags {
        grid-template-columns: 1fr;
    }
}
</style>