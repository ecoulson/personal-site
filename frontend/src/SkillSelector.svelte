<script>
    import { createEventDispatcher } from "svelte"

    let options = ["frontend", "backend", "infrastructure"]
    let selected = options[0];
    let dispatch = createEventDispatcher();

    function capitalize(str) {
        return str.charAt(0).toUpperCase() + str.substring(1, str.length).toLowerCase();
    }

    function onSkillSelected(option) {
        return () => {
            selected = option
            dispatch('skill-selected', option)
        }
    }
</script>

<div class="skill-option-container">
    {#each options as option}
        <h3 class:skill-option--active={option === selected} 
            class="skill-option" 
            on:click={onSkillSelected(option)}>
            {capitalize(option)}
        </h3>
    {/each}
</div>

<style>
    .skill-option-container {
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
        box-sizing: border-box;
    }
    .skill-option {
        color: #50B2C0;
        font-size: 32px;
        margin: 15px 15px;
    }
    .skill-option:hover {
        cursor: pointer;
    }
    .skill-option--active {
        text-decoration: underline;
    }
</style>
