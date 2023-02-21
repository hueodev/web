<script>
  import data from "../data.json";
</script>

<div class="container">
    <div class="text">
        <h1>{data.name}</h1>
        <p>{data.title}</p>
        <p>A self taught Web Developer / Designer from Sweden i am experienced in Svelte, Tailwind CSS, JavaScript, Typescript, SASS and HTML + CSS. Hit me up if you want a website or just want to ask a question.</p>
    </div>
    <img class="logo" src={data.image} height="160" width="160" alt="">
</div>

<style lang="scss">
.container {
    position: relative;
    display: flex;
    margin: auto;
    padding: 3.6rem 2rem 2rem 2rem;
    max-width: 45rem;    
}

.text {
    text-align: left;
    margin-right: 1.6rem;
    h1 {
        font-size: 36px;
        margin-bottom: 0.4rem;
    }
    p {
        font-size: 20px;
        margin-bottom: 0.6rem;
        color: rgb(212, 212, 216);
    }
}

.logo {
    border-radius: 100px;
    margin: 1.2rem 0rem;
}

@media (max-width: 668px) {
    .container {
        margin-top: -1.6rem;
        flex-direction: column-reverse;
        text-align: left;
    }
    .logo {
        margin-bottom: 1.6rem;
    }
}
</style>