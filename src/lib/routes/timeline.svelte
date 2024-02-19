<script lang="ts">
    import TimelineEnd from "./timeline-end.svelte";
    import TimelineStart from "./timeline-start.svelte";
</script>

<section>
    <div>
        <TimelineStart />
        <slot />
        <TimelineEnd />
    </div>
</section>

<style>
    section {
        width: 100%;

        display:flex;
        align-items: center;
        justify-content: center;
    }

    div{
        width:90%;
        display: flex;
        flex-direction: column-reverse;
    }

    /*mobile*/
    @media (min-width: 576px) {
        div{
            width:90%;
        }
    }

    /*large desktop*/
    @media only screen and (min-width: 1200px){
        div{
            width:85%;
        }
    }
</style>
