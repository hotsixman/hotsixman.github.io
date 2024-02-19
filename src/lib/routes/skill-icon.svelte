<script lang="ts">
    import { getContext } from "svelte";

    export let src: string;
    export let description: string = "";
    export let color:string|undefined = undefined;

    const setSkillDescription: (p1: string, p2?:string) => void = getContext(
        "setSkillDescription",
    );
</script>

<img
    {src}
    alt="skill icon"
    on:mouseover={() => {
        if (description && setSkillDescription) {
            setSkillDescription(description, color);
        }
    }}
    on:mouseout ={() => {
        if(description && setSkillDescription){
            setSkillDescription('');
        }
    }}
    on:focus={() => {}}
    on:blur={() => {}}
/>

<style>
    img {
        width: 40px;
        height: 40px;

        transition: transform 0.2s;
    }

    img:not(:hover) {
        filter: grayscale(1);
    }

    img:hover {
        transform: scale(1.3);
    }
</style>
