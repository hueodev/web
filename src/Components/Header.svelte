<script>
    let name = "Hugo"
    let title = "Student Webdevloper"
    let desc = "A self-taught Web Developer / Designer from Sweden who loves to create beautiful and functional websites and applications that deliver a great user experience. To get in touch click "
    let logo = "http://avatars.githubusercontent.com/u/78303660?v=4"
</script>

<div class="container">
    <div class="text">
        <h1>{name}</h1>
        <p>{title}</p>
        <p>{desc}<a href="mailto:hi@ogooo.dev">Here</a></p>
    </div>
    <img class="logo" src={logo} height="160" width="160" alt="">
</div>

<style lang="scss">
.container {
    position: relative;
    display: flex;
    margin: auto;
    padding: 6rem 2rem 1.8rem 2rem;
    max-width: 45rem; 
}

.text {
    text-align: left;
    margin-right: 1.6rem;
    p {
        font-size: 1.25rem;
        margin-bottom: 0.5rem;
        font-weight: 500;
        color: rgb(212, 212, 216);
        a {
            color: #fff;
            text-decoration: underline;
        }
    }
}

.logo {
    border-radius: 3rem;
    margin: 1rem 0rem 0rem;
}

@media (max-width: 668px) {
    .container {
        margin-top: -3.2rem;
        flex-direction: column-reverse;
        text-align: left;
    }
    .logo {
        margin-bottom: 1.6rem;
    }
}
</style>