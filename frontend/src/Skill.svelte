<script>
    import { fly } from "svelte/transition";
    import { quadInOut } from "svelte/easing";

    const DURATION = 400;
    const DELAY = DURATION;
    const X_TRANSLATION = 1000;
    const Y_TRANSLATION = 0;
    const OPACITY = 0;

    function getTransitionParameters(isTransitioningIn) {
        const parameters = {
            duration: DURATION,
            y: Y_TRANSLATION,
            opacity: OPACITY,
            easing: quadInOut
        }
        if (isTransitioningIn) {
            parameters["x"] = X_TRANSLATION;
            parameters["delay"] = DELAY;
        } else {
            parameters["x"] = -X_TRANSLATION;
            parameters["delay"] = 0;
        }
        return parameters;
    }

    export let skills;
    export let skillType;
</script>

<div
    in:fly={getTransitionParameters(true)}
    out:fly={getTransitionParameters(false)}
    class="skill-section" 
    id="{skillType.toLowerCase()}"
    >
    {#each skills as skill}
        <div class="skill-container">
            <img class="skill-logo" src="./assets/logos/{skill.src}" alt="Logo for {skill.name}" />
            <span class="skill-name">{skill.name}</span>
        </div>
    {/each}
</div>

<style>
    .skill-section {
        display: flex;
        max-width: 100%;
        flex-wrap: wrap;
    }

    .skill-name {
        font-size: 22px;
        font-size: clamp(16px, 2vw, 22px);
        margin-bottom: 15px;
    }

    .skill-container {
        width: 95px;
        display: flex;
        margin: 0px 15px;
        box-sizing: border-box;
        flex-direction: column;
        justify-content: center;
    }

    .skill-logo {
        display: block;
        margin: 5px auto;
        width: 85px;
        height: 85px;
        object-fit: contain;
    }
</style>