<script>
    import ProjectContainer from "./project-container.svelte";
    import Project from "./project.svelte";

    import taikowiki from "../../../assets/projects/taikowiki.png";
    import taikowikiNew from "../../../assets/projects/taikowiki-new.png";
</script>

<ProjectContainer>
    <Project title="(구)태고의 달인 한국어 위키" src={taikowiki} />
    <Project title="node-hiroba" />
    <Project
        title="태고의 달인 위키"
        src={taikowikiNew}
        href="//taiko.wiki"
    />
</ProjectContainer>
