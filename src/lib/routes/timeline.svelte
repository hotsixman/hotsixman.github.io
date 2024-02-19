<script lang="ts">
    import Section from "./section.svelte";
    import TimelineStart from "./timeline-start.svelte";
    import TimelineEnd from "./timeline-end.svelte";
</script>

<Section title="Timeline">
    <TimelineStart />
    <slot />
    <TimelineEnd />
</Section>
