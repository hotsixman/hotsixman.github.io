<script lang="ts">
    export let src:string = '';
    export let text:string;
    export let href = '/';
</script>

<a href={`/#${href}`} class="logo">
    {#if src}
    <img class="logo-img" {src} alt="hotsix logo" />
    {/if}
    <span class="logo-text">{text}</span>
</a>

<style>
    .logo{
        height:100%;
        display: flex;
        flex-direction: row;
        align-items: center;

        text-decoration: none;
    }

    .logo-img {
        width: 60px;
    }

    .logo-text {
        font-family: "Actor";
        font-weight: bold;
        font-size: 20px;
        color:white !important;
    }
</style>