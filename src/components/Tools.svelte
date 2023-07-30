<div class="container">
  <h1>Technologies</h1>
  <div class="content">
    <h1>Languages</h1>
    <div class="content-lang">
      <a href="https://" target="_blank">CSS / HTML</a>
      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank">Javascript</a>
      <a href="https://developer.mozilla.org/en-US/docs/Glossary/SQL" target="_blank">SQL</a>
      <a href="https://sass-lang.com" target="_blank">SCSS</a>
    </div>
    <h1>Frameworks</h1>
    <div class="content-frame">
      <a href="https://svelte.dev" target="_blank">Svelte.js</a>
      <a href="https://kit.svelte.dev" target="_blank">SvelteKit.js</a>
      <a href="https://nodejs.org" target="_blank">Node.js</a>
      <a href="https://www.prisma.io" target="_blank">Prisma</a>
      <a href="https://tailwindcss.com" target="_blank">Tailwind CSS</a>
    </div>
    <h1>Tools & Platforms</h1>
    <div class="content-tools">
      <a href="https://github.com" target="_blank">Github</a>
      <a href="https://code.visualstudio.com" target="_blank">Visual Studio Code</a>
      <a href="https://cpanel.net" target="_blank">CPanel</a>
      <a href="https://pages.cloudflare.com" target="_blank">Cloudflare Pages</a>
    </div>
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
    }
  }

  .content {
    h1 {
      margin: 0.5rem 0 0;
      color: rgb(163, 163, 163);
    }
    .content-lang, .content-frame, .content-tools {
      display: flex;
      gap: .7rem;
      margin: .3rem 0;
      flex-wrap: wrap;
      a {
        font-size: .8rem;
        font-weight: 500;
        padding: .2rem .4rem;
        border-radius: 4px;
        text-decoration: none;
        color: rgb(163, 163, 163);
        border: 1px solid rgb(75, 132, 182);
        transition: all 300ms ease-in-out;
        &:hover {
          background-color: rgb(75, 132, 182);
          color: rgb(255, 255, 255);
        }
      }
    }
  }
</style>