<script>
    import { tooltip } from 'svooltip';
	import 'svooltip/styles.css';

    let links = [
		{ name: "Email", tooltip:"hi@ogooo.dev", url: "mailto:hi@ogooo.dev" }, 
		{ name: "Github", tooltip:"Ogooooo", url: "http://github.com/ogooooo" },
        { name: "Discord", tooltip:"Ogooo#7072", url: "" }
	];
</script>

<div class="container">
    <div class="text">
        <h1>Get in Touch</h1>
        <p>If you'd like to collab on a small project or just want to say hello, feel free to send me an email.</p>
    </div>
    <div class="tags">
        {#each links as link}
            <a href={link.url} target="_blank" rel="noopener noreferrer" use:tooltip={{content: link.tooltip, placement: "bottom", offset: 12, html: true}}>{link.name}</a>
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
    gap: .6rem;
    grid-template-columns: auto auto auto;
    margin: 1rem 0rem 1rem 0rem;
    a {
        max-width: 40rem;
        padding: .4rem 0rem;
        text-align: center;
        font-size: 20px;
        border-radius: .6rem;
        background: rgb(29, 29, 32);
        border-radius: 6px;
        text-decoration: none;
        color: rgb(255, 255, 255);
        border: 2px solid rgb(33, 33, 37);
        transition: 400ms ease-in-out;
        &:hover {
            border: 2px solid rgb(42, 77, 136);
            // transform: scale(1.02);
        }
    }
}

@media (max-width: 668px) {
    .tags {
        grid-template-columns: 1fr;
    }
}
</style>