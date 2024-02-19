<script lang="ts">
    export let position:'top'|'bottom';
</script>

<div class="timeline-line" style={`height:${position==='top'?'8px':'calc(100% - 24px)'};`}/>

<style>
    .timeline-line{
        width:4px;

        background-color:#8ffcff;
    }
</style>