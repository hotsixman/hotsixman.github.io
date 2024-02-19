<script lang="ts">
    import { onMount } from "svelte";

    export let title:string = '';

    let section:HTMLElement;
    let content:HTMLElement;

    onMount(() => {
        let callback = (entries:IntersectionObserverEntry[]) => {
            entries.forEach(e => {
                if(e.isIntersecting){
                    setTimeout(() => {
                        content.style.opacity = "1";
                    }, 500);
                    (e.target as HTMLElement).style.transform = "translateX(0)";
                    (e.target as HTMLElement).style.opacity = "1";
                }
            })
        }
        let observer = new IntersectionObserver(callback);
        observer.observe(section);
    })
</script>

<section bind:this={section}>
    <div class="title">
        {title}
    </div>
    <div bind:this={content}>
        <slot/>
    </div>
</section>

<style>
    section {
        width: 100%;

        display:flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        transform: translateX(25%);
        transition: transform 0.5s ease, opacity 0.5s ease;
        opacity: 0;

        overflow-y:hidden;
    }

    div{
        width:90%;
        display: flex;
        flex-direction: column;
    }

    .title{
        font-size:45px;
        font-weight: bolder;
        font-family:'Actor';
    }

    div:not(.title){
        opacity: 0;
        transition: opacity 0.5s;
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
