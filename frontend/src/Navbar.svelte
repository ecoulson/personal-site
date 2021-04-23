<script lang="ts"> 
    import { links } from "svelte-routing";
</script>

<nav use:links>
    <div class="nav-group main-group">
        <a href="/">Evan Coulson</a>
    </div>
    <div class="nav-group page-group">
        <a href="/about">About</a>
        <a href="/projects">Projects</a>
    </div>
</nav>

<style>
    nav {
        box-sizing: border-box;
        width: 100%;
        height: 75px;
        padding: 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #FAAA8D;
    }
    .nav-group {
        display: flex;
    }
    .main-group {
        font-size: 28px;
    }
    .page-group {
        font-size: 24px;
    }
    a {
        color: #201E1F;
        margin: 0 25px;
    }
</style>