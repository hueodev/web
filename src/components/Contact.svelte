<div class="container">
  <h1>Links</h1>
  <div class="content-links">
    <p>Github</p><a href="https://github.com/hueodev" target="_blank">@hueodev</a>
    <p>Discord</p><a href="https://discordapp.com/users/420661585007083520" target="_blank">@hueo</a>
    <p>Email</p><a href="/">@hueo</a>
  </div>
</div>

<style lang="scss">
  .container {
    max-width: 28rem;
    margin: 2rem auto;
    h1 {
      font-size: 1rem;
      font-weight: 500;
      margin: 0 0 0.8rem 0;
    }
  }

  .content-links {
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 4rem;
    row-gap: 0.2rem;
    p {
      font-size: 1rem;
      color: rgb(128, 128, 128);
    }
    a {
      color: rgb(210, 213, 218);
      text-decoration: none;
      font-weight: 500;
      transition: all 250ms;
      width: fit-content;
        &:hover {
          color: rgb(149, 152, 157);
      }
    }
  }
</style>
