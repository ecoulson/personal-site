<script>
    import Skill from "./Skill.svelte"

    let frontendSkills = [
        {src: "./react-logo.png", name: "React"},
        {src: "./html-logo.png", name: "HTML"},
        {src: "./css-logo.png", name: "CSS"},
        {src: "./js-logo.png", name: "JS"},
        {src: "./svelte-logo.png", name: "Svelte"},
        {src: "./redux-logo.png", name: "Redux"},
    ]
    let backendSkills = [
        {src: "./ts-logo.png", name: "TS"},
        {src: "./node-logo.png", name: "Node.js"},
        {src: "./express-logo.png", name: "Express"},
        {src: "./mongo-logo.png", name: "MongoDB"},
        {src: "./java-logo.png", name: "Java"},
        {src: "./sql-logo.png", name: "SQL"},
        {src: "./csharp-logo.png", name: "C#"},
        {src: "./redis-logo.png", name: "Redis"},
        {src: "./python-logo.png", name: "Python"},
    ]
    let infrastructureSkills = [
        {src: "./docker-logo.png", name: "Docker"},
        {src: "./kubernetes-logo.png", name: "Kubernetes"},
        {src: "./aws-logo.png", name: "AWS"},
        {src: "./azure-logo.jpeg", name: "Azure"},
        {src: "./cloud-logo.png", name: "Cloud"},
        {src: "./heroku-logo.png", name: "Heroku"},
        {src: "./git-logo.png", name: "Git"},
        {src: "./circleci-logo.png", name: "CircleCI"},
    ]
</script>

<section class="skills">
    <h2 class="skills-header">Skills</h2>
    <Skill skills={frontendSkills} skillType="frontend" />
    <Skill skills={backendSkills} skillType="backend" />
    <Skill skills={infrastructureSkills} skillType="infrastructure" />
</section>

<style>
    .skills {
        grid-area: skills;
    }
    .skills-header {
        text-align: left;
        margin: 0;
        margin-left: 25px;
        text-decoration: underline;
        font-size: 40px;
        font-size: clamp(28px, 5vw, 40px);
    }
</style>