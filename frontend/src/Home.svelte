<script>
    import About from "./About.svelte";
    import Skills from "./Skills.svelte";
</script>

<main class="home">
    <div class="home-wrapper">
        <About />
        <Skills />
    </div>
</main>

<style>
    .home {
        background-color: #FEEFDD;
        min-height: 100vh;
        min-height: calc(100vh - 75px);
        width: 100vw;
        box-sizing: border-box;
    }
    .home-wrapper {
        margin: 0 auto;
        max-width: 1000px;
        display: grid;
        grid-template-areas: 
            "about"
            "skills"
            "experience"
            "contact";
    }
</style>