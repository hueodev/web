<div class="container">
    <div class="text">
        <h1>Hugo</h1>
        <p>Student Webdevloper</p>
        <p>A self-taught Web Developer / Designer from Sweden who loves to create beautiful and functional websites and applications that deliver a great user experience. When I'm not busy with projects or schoolwork, I usually watch movies.</p>
    </div>
    <img class="logo" src="http://avatars.githubusercontent.com/u/78303660?v=4" height="160" width="160" alt="">
</div>

<style lang="scss">
.container {
    position: relative;
    display: flex;
    margin: auto;
    padding: 3rem 2rem 2rem 2rem;
    max-width: 45rem;    
}

.text {
    text-align: left;
    margin-right: 1.6rem;
    h1 {
        margin-bottom: 0.6rem;
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