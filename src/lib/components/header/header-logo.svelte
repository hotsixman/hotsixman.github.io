<script lang="ts">
    import { link } from "svelte-routing";
    export let src:any;
    export let text:string;
</script>

<a href="/" use:link class="logo">
    <img class="logo-img" {src} alt="hotsix logo" />
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