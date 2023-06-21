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
    <div class="about">
        <h1>About</h1>
        <p><span>{getGreeting()}</span> Im Hugo. I enjoy buildning dynamic and creative webbsites from start to finnish. I aim to approach every problem with a fresh out-of-the-box perspective. Hoping to get better and improve what i do, wish me luck!</p>    
    </div>
    <div class="work">
        <h1>Work Experience</h1>
        <p>I have been working on some small projects but if you want something done just contact me.</p>
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
        color: #4b84b6;
    }
</style>
