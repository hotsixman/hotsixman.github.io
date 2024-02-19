<script lang="ts">
    import { onMount } from "svelte";
    import Profile from "./profile.svelte";
    import ProfileContent from "./profile-content.svelte";

    let container: HTMLElement;
    let title: HTMLElement;

    onMount(() => {
        let callback = (entries: IntersectionObserverEntry[]) => {
            entries.forEach((e) => {
                if (e.isIntersecting) {
                    (title as HTMLElement).style.transform = "translateY(0)";
                    (title as HTMLElement).style.opacity = "1";
                }
            });
        };
        let observer = new IntersectionObserver(callback);
        observer.observe(container);
    });
</script>

<div class="container" bind:this={container}>
    <div class="title" bind:this={title}>
        그냥<br />이상한 사람
    </div>
    <Profile>
        <ProfileContent item="Nickname" content="핫식스맨" />
        <ProfileContent item="Birthday" content="2005 02 25" />
        <ProfileContent content="Studying web developing..." />
    </Profile>
</div>

<style>
    .container {
        width: 100%;

        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        column-gap: 40px;

        margin-top:20px;
        margin-bottom: 50px;
    }

    .title {
        text-align: center;

        transform: translateY(300px);
        opacity: 0;
        transition:
            transform 0.5s ease,
            opacity 0.5s ease;

        font-family: "Black Han Sans";
        font-size: 100px;
        font-weight: normal;

        text-wrap: pretty;
    }
</style>
