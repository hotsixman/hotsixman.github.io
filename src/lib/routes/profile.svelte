<script lang="ts">
    import { onMount } from "svelte";
    import hotsix from "../../assets/hotsix.png";

    let profile: HTMLElement;

    onMount(() => {
        let callback = (entries: IntersectionObserverEntry[]) => {
            entries.forEach((e) => {
                if (e.isIntersecting) {
                    setTimeout(() => {
                        (profile as HTMLElement).style.transform =
                            "translateX(0)";
                        (profile as HTMLElement).style.opacity = "1";
                    }, 500);
                }
            });
        };
        let observer = new IntersectionObserver(callback);
        observer.observe(profile);
    });
</script>

<div class="profile" bind:this={profile}>
    <img src={hotsix} alt="profile" />
    <slot />
</div>

<style>
    .profile {
        max-width: calc(100% - 20px);
        width: 500px;
        height: 330px;

        box-sizing: border-box;
        border: 5px solid #00f9ff;
        border-radius: 15px;

        display: flex;
        flex-direction: column;
        align-items: center;

        transform: translateX(200px);
        opacity: 0;
        transition:
            transform 0.5s ease,
            opacity 0.5s ease;

        box-shadow: 0 0 20px #57fcff;
    }

    .profile:hover{
        border: 5px solid #04ff00;
        box-shadow: 0 0 20px #4dff53;
    }

    img {
        width: 150px;
        height: 150px;

        background-color: #d0fdff;
        border-radius: 50%;

        margin-top: 20px;
        margin-bottom: 30px;
    }
</style>
