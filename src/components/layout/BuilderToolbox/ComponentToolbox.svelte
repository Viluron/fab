<script lang="ts">
    import Toolbox from "../../fabUiComponents/Toolbox.svelte";
import ComponentTile from "./ComponentTile.svelte";

    export let height = "unset";

    let components = [
        {
            name: 'FlexBox',
            description: '💪 Mega Flex',
            id: 'flexbox',
            properties: {
                id: {
                    type: 'string',
                    default: ''
                },
                direction: {
                    type: 'enum',
                    default: 'row',
                    values: [
                        'row', 'column'
                    ]
                }
            }
        },
        {
            name: 'Button',
            description: 'Lol eins button',
            id: 'button',
        },
        {
            name: 'Input',
            description: 'Put you dick in here',
            id: 'input'
        }
    ];


</script>

<template>
    <Toolbox title="Components" {height}>
        <slot>
            {#each components as comp}
                <ComponentTile title={comp.name} description={comp.description} compId={comp.id}/>
            {/each}
        </slot>
    </Toolbox>
</template>

<style lang="less">
</style>