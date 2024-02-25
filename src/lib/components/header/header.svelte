<script lang="ts">
    import HeaderIcon from "./header-icon.svelte";
    import HeaderLeft from "./header-left.svelte";
    import HeaderRight from "./header-right.svelte";
    import HeaderLogo from "./header-logo.svelte";

    import hotsix from "../../../assets/hotsix.png";
    import discord from '../../../assets/discord.svg';
    import email from '../../../assets/email.svg';
    import github from '../../../assets/github.svg'

    let header:HTMLElement;
    let oldscroll = window.scrollY;
    window.addEventListener('scroll', (event) => {
        if(oldscroll > window.scrollY){
            header.style.transform = `translateY(${window.scrollY}px)`;
        }
        oldscroll = window.scrollY;
    })
</script>

<header bind:this={header}>
    <HeaderLeft>
        <HeaderLogo src={hotsix} text="Hotsixman"/>
        <HeaderLogo text="Projects" href="/projects"/>
    </HeaderLeft>
    <HeaderRight>
        <HeaderIcon href="https://github.com/hotsixman" src={github}/>
        <HeaderIcon href="https://discordapp.com/users/1208793739779379220" src={discord}/>
        <HeaderIcon href="mailto:hotsixman05@gmail.com" src={email}/>
    </HeaderRight>
</header>

<style>
    header {
        height: 60px;

        padding-inline-start: 10px;
        padding-inline-end: 20px;

        background-color: #0f0057;

        display: flex;
        flex-direction: row;
        align-items: center;
        
        position:relative;

        z-index: 2;
    }
</style>
