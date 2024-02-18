<script lang="ts">
    export let src:string;
    export let href:string;
</script>

<a {href}>
    <img {src} alt="icon"/>
</a>

<style>
    img{
        width:30px;
        height:30px;
    }
</style>