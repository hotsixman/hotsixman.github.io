<script lang="ts">
    export let width:string = "30%";
</script>

<div class="left" style={`width:${width};`}>
    <slot/>
</div>

<style>
    .left{
        display:flex;
        flex-direction: row;
        align-items: center;
        column-gap: 10px;
    }
</style>