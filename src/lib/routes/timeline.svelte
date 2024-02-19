<script lang="ts">
    import Section from "./section.svelte";
    import TimelineStart from "./timeline-start.svelte";
    import TimelineEnd from "./timeline-end.svelte";
</script>

<Section title="Timeline">
    <div class="reverse">
        <TimelineStart />
        <slot />
        <TimelineEnd />
    </div>
</Section>

<style>
    .reverse{
        width:100%;

        display:flex;
        flex-direction: column-reverse;
    }
</style>