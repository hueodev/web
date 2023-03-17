<script>
    import { useLanyard } from "svelte-lanyard";
	const data = useLanyard("420661585007083520", { type: 'rest', restInterval: 1e3 });
</script>

<main class="container">
  <div class="box">
    {#if $data && $data.listening_to_spotify }
        <p><svg stroke="currentColor" fill="#1ED760" stroke-width="0" viewBox="0 0 16 16" height="1.2rem" width="1.2rem" xmlns="http://www.w3.org/2000/svg"><path d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0zm3.669 11.538a.498.498 0 0 1-.686.165c-1.879-1.147-4.243-1.407-7.028-.77a.499.499 0 0 1-.222-.973c3.048-.696 5.662-.397 7.77.892a.5.5 0 0 1 .166.686zm.979-2.178a.624.624 0 0 1-.858.205c-2.15-1.321-5.428-1.704-7.972-.932a.625.625 0 0 1-.362-1.194c2.905-.881 6.517-.454 8.986 1.063a.624.624 0 0 1 .206.858zm.084-2.268C10.154 5.56 5.9 5.419 3.438 6.166a.748.748 0 1 1-.434-1.432c2.825-.857 7.523-.692 10.492 1.07a.747.747 0 1 1-.764 1.288z"></path></svg>Playing <a href="https://open.spotify.com/track/{$data.spotify.track_id}">{$data.spotify.song} - {$data.spotify.artist}</a></p>
    {:else}
        <p><svg stroke="currentColor" fill="#1ED760" stroke-width="0" viewBox="0 0 16 16" height="1.2rem" width="1.2rem" xmlns="http://www.w3.org/2000/svg"><path d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0zm3.669 11.538a.498.498 0 0 1-.686.165c-1.879-1.147-4.243-1.407-7.028-.77a.499.499 0 0 1-.222-.973c3.048-.696 5.662-.397 7.77.892a.5.5 0 0 1 .166.686zm.979-2.178a.624.624 0 0 1-.858.205c-2.15-1.321-5.428-1.704-7.972-.932a.625.625 0 0 1-.362-1.194c2.905-.881 6.517-.454 8.986 1.063a.624.624 0 0 1 .206.858zm.084-2.268C10.154 5.56 5.9 5.419 3.438 6.166a.748.748 0 1 1-.434-1.432c2.825-.857 7.523-.692 10.492 1.07a.747.747 0 1 1-.764 1.288z"></path></svg>Not listening to anything!</p>
    {/if}
  </div>
</main>

<style lang="scss">
.container {
  position: relative;
  margin: auto;
  max-width: 45rem;
  padding: 0rem 2rem 2rem 2rem;
}

.box {
    display: flex;
    flex-wrap: wrap;
}

a {
    text-decoration: none; 
    color: #48a548;
    &:hover {
        text-decoration: underline 2px;
        text-decoration-color: #48a548;
    }
}

p {
    font-weight: 600;
    text-align: center;
    font-size: 1.1rem;
    color: #48a548;
    background: rgb(29, 29, 32);
    padding: .5rem 1.9rem .5rem 1.4rem;
    width: 45rem;
    border: 2px solid rgb(33, 33, 37);
    border-radius: .2rem;
}

svg {
    margin: -.17rem .3rem;
}
</style>
