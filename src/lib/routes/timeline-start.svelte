<script lang="ts">
    import TimelineCircle from "./timeline-circle.svelte";
    import TimelineLine from "./timeline-line.svelte";
</script>

<article>
    <div class="timeline">
        <div class="timeline-margin"/>
        <TimelineCircle/>
        <TimelineLine position="top"/>
    </div>
    <div class="title">
        2005. 2. 25.
    </div>
</article>

<style>
    article{
        width:100%;
        height:max-content;

        display:flex;
        flex-direction: row;
        align-items: stretch;
        justify-content: center;
    }

    .timeline{
        width:20px;

        display:flex;
        flex-direction: column-reverse;
        align-items: center;
        justify-content: center;
    }

    .timeline-margin{
        height:8px;
    }

    .title{
        width:calc(100% - 40px);
        height:32px;
        font-size:20px;
        font-weight: bold;

        display:flex;
        flex-direction: row;
        align-items: center;

        margin-left:20px;

        transform: translateY(1px);
    }
</style>