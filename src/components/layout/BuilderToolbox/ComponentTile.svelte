<script lang="ts">

    export let title: string;
    export let description: string;
    export let compId: string;

</script>

<section class="comp">
    <h1>
        {title}
    </h1>
    <p>
        {description}
    </p>
</section>

<style lang="less">
    .comp {
        width: 10em;
        border-radius: 5px;
        transition: 0.3s;

        &:hover {
            background-color: var(--hover-color);
        }
    }
</style>