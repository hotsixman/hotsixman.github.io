<script lang="ts">
    import TimelineCircle from "./timeline-circle.svelte";
    import TimelineLine from "./timeline-line.svelte";

    export let href: string|undefined = undefined;
    export let date: string = '';
</script>

<a {href}>
    <div class="timeline">
        <TimelineLine position="top" />
        <TimelineCircle />
        <TimelineLine position="bottom" />
    </div>
    <div class="text">
        <div class="title">
            <slot/>
        </div>
        {#if date}
            <div class="date">
                {date}
            </div>
        {/if}
    </div>
</a>

<style>
    a {
        width:100%;
        height: max-content;

        display: flex;
        flex-direction: row;
        align-items: stretch;
        justify-content: center;

        text-decoration: none;
    }

    .timeline {
        width: 20px;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .text {
        width: calc(100% - 40px);

        margin-left: 20px;
    }

    .title {
        height: 32px;
        font-size: 20px;
        font-weight: bold;

        display: flex;
        flex-direction: row;
        align-items: center;

        transform: translateY(1px);

        color:white;
    }

    .date {
        font-size: 13px;
        color: rgb(180, 180, 180);
    }
</style>
