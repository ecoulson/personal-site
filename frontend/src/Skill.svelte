<script>
    export let skills;
    export let skillType;

    function capitalize() {
        return skillType.charAt(0).toUpperCase() + skillType.substring(1, skillType.length).toLowerCase();
    }
</script>

<div class="skill-section" id="{skillType.toLowerCase()}">
    <h3 class="skill-section-title">{capitalize()}</h3>
    <div class="skill-icons">
        {#each skills as skill}
            <div class="skill-container">
                <img class="skill-logo" src={skill.src} alt="Logo for {skill.name}" />
                <span class="skill-name">{skill.name}</span>
            </div>
        {/each}
    </div>
</div>

<style>

    .skill-icons {
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

    .skill-section-title {
        color: #50B2C0;
        font-size: 32px;
    }
</style>