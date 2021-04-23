<main class="home">
    <img class="profile-picture" alt="Profile shot of Evan Coulson" src="./me.jpg" />
    <p class="about-me-text"></p>
</main>

<style>
    .about-me-text {
        grid-area: "about-text";
    }
    .profile-picture {
        grid-area: "profile-pciture";
        width: 250px;
        height: 250px;
        margin: 15px;
        border-radius: 100%;
        object-fit: cover;
        border: 3px solid #50B2C0;
    }
    .home {
        background-color: #FEEFDD;
        height: 100vh;
        width: 100vw;
        box-sizing: border-box;
        display: grid;
        grid-template-areas:
            "profile-picture    about-text      about-text      "
            "frontend-skills    backend-skills  dev-ops skills  ";
    }
</style>