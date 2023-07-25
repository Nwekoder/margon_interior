<script lang="ts">
    export let path:Array<string>;

    function Capitalize(input: string) {
        return input.slice(0,1).toUpperCase() + input.slice(1)
    }
</script>

<ul class="flex gap-1">
    {#each path as p,i}
        {#if i !== path.length - 1}
            <li class="">
                <a href="/{p}">
                    {Capitalize(p)}
                </a>
            </li>
        {:else}
            <li class="">
                {Capitalize(p)}
            </li>
        {/if}
    
        {#if i !== path.length - 1 && i !== 0}
            <li>/</li>
        {/if}
    {/each}
</ul>