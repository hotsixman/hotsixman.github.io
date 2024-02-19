<script lang="ts">
    import { setContext } from "svelte";
    import Section from "./section.svelte";

    let description: string = "";
    let textColor: string = "white";

    function setSkillDescription(text: string, color: string = "white") {
        description = text;
        textColor = color;
    }

    setContext("setSkillDescription", setSkillDescription);
</script>

<Section title="Skills">
    <div class="description" style={`color:${textColor};`}>
        {#if description}
            {description}
        {/if}
    </div>
    <div class="skills-container">
        <slot />
    </div>
</Section>

<style>
    .description {
        font-size: 30px;
        font-family: "Dongle";

        min-height:30px;

        display: flex;
        flex-direction: row;
        align-items: center;

        line-height: 80%;
    }

    /*mobile*/
    @media only screen and (max-width: 767px) {
        .description {
            padding-inline-start: 0px;
            height: 50px;
        }
    }

    /*large desktop*/
    @media only screen and (min-width: 768px) {
        .description {
            padding-inline-start: 20px;
            height:30px;
        }
    }
</style>
