<script>
  import { onMount } from "svelte";

  let repos;

  onMount(async () => {
    const response = await fetch("https://gh-pinned-repos.egoist.dev/?username=hueodev");
    repos = await response.json();
  });
</script>

<div class="container">
  <h1>Featured Work</h1>
  <div class="repos">
  {#if repos}
      {#each repos as { link, owner, repo, description, languageColor, language, stars, forks }}
          <a href={link}>
              <h1>{repo}</h1>
              <p>{description}</p>
              <div class="info">
                  <span>{language}</span>
                  {#if stars}
                      <span class="icons"><img src="icons/star.svg" alt="icon"/>{stars}</span>
                  {/if}
                  {#if forks}
                      <span class="icons"><img src="icons/fork.svg" alt="icon"/>{forks}</span>
                  {/if}
              </div>
          </a>
      {/each}
  {/if}
  {#if !repos}
      <div class="loading">
        <span>Loading</span><img src="icons/spinner.svg" alt="">
      </div>
  {/if}
  </div>
</div>

<style lang="scss">
  .container {
    position: relative;
    max-width: 28rem;
    margin: auto;
    h1 {
      font-size: 1rem;
      font-weight: 500;
      margin: 0 0 0.5rem 0;
    }
  }

  .repos {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 0.6rem;
    h1 {
      font-size: 1rem;
      font-weight: 500;
    }
    p {
      font-size: 1rem;
      color: rgb(128, 128, 128);
      margin: 0.2rem 0 0.6rem;
    }
    a {
      display: flex;
      flex-direction: column;
      color: rgb(210, 213, 218);
      background: rgb(19, 19, 20);
      box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
      border: 1px solid #1b1b1c;
      transition: all 250ms;
      padding: 0.9rem;
      border-radius: 0.2rem;
      line-height: 1.4rem;
      text-decoration: none;
      cursor: pointer;
      &:hover {
        background: rgb(24, 24, 25);
      }
    }
  }

  .info {
    display: flex;
    gap: 0.4rem;
    margin-top: auto;
    img {
      height: 0.9rem;
      margin-right: 0.3rem;
      vertical-align: middle;
      display: inline-block;
    }
    span {
      font-size: 0.9rem;
      padding: 0.2rem 0.4rem;
      border-radius: 0.2rem;
      background: rgba(39, 39, 42, 0.387);
    }
  }

  .loading {
    display: flex;
    img {
      width: .86rem;
      color: rgb(128, 128, 128);
      margin-left: 0.4rem;
      vertical-align: middle;
      display: inline-block;
    }
    span {
      font-size: 0.94rem;
      color: whitesmoke;
    }
  }
</style>
