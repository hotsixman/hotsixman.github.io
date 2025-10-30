<script lang="ts">
    import Section from "../section.svelte";
</script>

<Section title="Projects">
    <div class="project-container">
        <slot/>
    </div>
</Section>

<style>
    .project-container{
        width:100%;
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));

        margin-top:10px;

        row-gap:8px;
        column-gap:3px;
    }
</style>