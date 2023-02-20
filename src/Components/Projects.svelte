<script>
    import data from "../data.json";
</script>

<div class="container">
    <div class="text">
        <h1>Projects</h1>
        <p>Below are some of my top open source projects that I both own and contribute to.</p>
    </div>
    <div class="projects">
        {#each data.projects as project}
            <a class="box" href={project.url} target="_blank" rel="noreferrer">
                <h1>{project.title}</h1>
                <ul class="tags">
                    {#each project.tags as tag}
                        <li>{tag}</li>
                    {/each}
                </ul>
                <p>{project.desc}</p>
            </a>
        {/each}
    </div>
</div>

<style lang="scss">
.container {
    position: relative;
    margin: auto;
    padding: 0rem 2rem;
    max-width: 45rem;
}

.text {
    h1 {
        font-size: 2.2rem;
        padding-bottom: .5rem;
    }
    p {
        font-size: 20px;
        color: rgb(212, 212, 216);
        margin-bottom: 1.6rem;
    }
}

.projects {
    position: relative;
    display: grid;
    gap: 1rem;
    grid-template-columns: 1fr 1fr;
}

.box {
    position: relative;
    max-width: 45rem;
    max-height: 15rem;
    border-radius: .4rem;
    padding: 1.4rem;
    text-decoration: none;
    border: 2px solid rgb(33, 33, 37);
    color: rgb(255, 255, 255);
    background: rgb(29, 29, 32);
    transition: 400ms ease-in-out;
    h1 {
        font-size: 1.4rem;
        font-weight: 400;
        margin-bottom: .6rem;
    }
    p {
        font-size: 1.125rem;
        color: #A1A1AA;
        margin-top: .6rem;
    }
    &:hover {
        border: 2px solid rgb(42, 77, 136);
        transform: scale(1.02);
    }
}

.tags {
    position: relative;
    display: inline;
    margin-bottom: .4rem;
    font-size: .96rem;
    li {
        display: inline;
        list-style-type: none;
        padding: 2px 8px;
        margin-right: .4rem;
        border-radius: .2rem;
        background: rgb(39, 39, 42);
    }
}

@media (max-width: 640px) {
    .projects {
        grid-template-columns: 1fr;
    }
}
</style>