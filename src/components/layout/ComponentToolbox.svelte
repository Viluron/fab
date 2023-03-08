<script lang="ts">
    import ComponentTile from "./ComponentTile.svelte";

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

<section class="flex-column toolbox">
    <slot>
        {#each components as comp}
            <ComponentTile title={comp.name} description={comp.description} compId={comp.id}/>
        {/each}
    </slot>
</section>

<style lang="less">
    .toolbox {
        height: 100%;
        width: 10em;
    }
</style>