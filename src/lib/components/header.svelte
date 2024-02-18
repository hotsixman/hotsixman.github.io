<script lang="ts">
    import hotsix from "../../assets/hotsix.png";
    import { link } from "svelte-routing";
</script>

<header>
    <a href="/" use:link class="logo">
        <img class="logo-img" src={hotsix} alt="hotsix logo" />
        <span class="logo-text">Hotsixman</span>
    </a>
</header>

<style>
    header {
        height: 60px;

        padding-inline: 10px;

        background-color: #0f0057;

        display: flex;
        flex-direction: row;
        align-items: center;
    }

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
