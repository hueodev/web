<script>
  function getGreeting() {
    const hour = new Date().getHours();

    if (hour >= 0 && hour < 12) {
      return "Good Morning,";
    } else if (hour >= 12 && hour < 18) {
      return "Good Afternoon,";
    } else {
      return "Good Evening,";
    }
  }
</script>

<div class="container">
  <div class="content-about">
    <h1>About</h1>
    <p>
      <span>{getGreeting()}</span> I'm Hugo. I enjoy building creative and innovative
      software from start to finish. I aim to approach every problem with a fresh
      out-of-the-box perspective. Hoping to get better and improve what I do.
    </p>
  </div>
  <div class="content-work">
    <h1>Experience</h1>
    <p>
      I have been involved in numerous projects, both big and small, where I
      mostly use Go. Additionally, I am currently expanding my skills by
      learning C. If you would like to reach out to me, please feel free to
      contact me via Email or Discord.
    </p>
  </div>
</div>

<style lang="scss">
  .container {
    display: grid;
    gap: 2rem;
    margin: 2rem auto;
    max-width: 28rem;
  }

  h1 {
    font-size: 1rem;
    font-weight: 500;
  }

  p {
    font-size: 1rem;
    color: rgb(163, 163, 163);
  }

  span {
    color: rgb(75, 132, 182);
  }
</style>
