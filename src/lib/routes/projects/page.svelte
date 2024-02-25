<script>
    import ProjectContainer from "./project-container.svelte";
    import Project from "./project.svelte";

    import taikowiki from '../../../assets/projects/taikowiki.png';

</script>
<ProjectContainer>
    <Project title="태고의 달인 한국어 위키" src={taikowiki} href="/projects/taikowiki"/>
    <Project title="node-hiroba"/>
</ProjectContainer>