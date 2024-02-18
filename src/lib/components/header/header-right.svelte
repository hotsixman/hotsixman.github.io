<div class="right">
    <slot/>
</div>

<style>
    .right{
        flex: 1 0 auto;
        display:flex;
        flex-direction: row-reverse;
        align-items: center;

        column-gap: 10px;
    }
</style>