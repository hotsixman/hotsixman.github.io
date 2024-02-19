<script lang="ts">
    export let groupName:string;
</script>

<div class="skill-group-container">
    <div class="group-name">
        {groupName}
    </div>
    <div class="skills">
        <slot/>
    </div>
</div>

<style>
    .skill-group-container{
        width:100%;
        display:flex;
        flex-direction: column;
    }

    .group-name{
        font-size:30px;
        font-weight: bold;
    }

    .skills{
        height:50px;

        display:flex;
        flex-direction: row;
        overflow:visible;
        align-items: center;

        column-gap: 8px;
    }
</style>