<script lang="ts">
    export let item:string = '';
    export let content:string;
</script>

<div class="profile-content">
    {#if item}
    <span style="font-weight: bold">{item}</span>
    : 
    {/if}
    {content}
</div>

<style>
    .profile-content{
        margin-top:5px;
        margin-bottom: 5px;
    }
</style>