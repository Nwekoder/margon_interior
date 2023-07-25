<script lang="ts">
    let active = 'deskripsi'

    function changeTab(tab: string) {
        active = tab
    }

    const inactive_class = 'border-x border-x-stone-400 border-t-stone-400 border-t'
    const active_class = 'border-x border-x-orange-500 bg-orange-500 text-white border-t-orange-500 border-t'

    function is_active(tab:string) {
        return tab == active
    }
</script>

<div class="flex gap-2 border-b-orange-500 border-b">
    <button on:click={() => changeTab('deskripsi')} class="px-4 py-2 rounded-t-md {active == 'deskripsi' ? active_class : inactive_class}">Deskripsi</button>
    <button on:click={() => changeTab('ulasan')} class="px-4 py-2 rounded-t-md {active == 'ulasan' ? active_class : inactive_class}">Ulasan</button>
</div>

<div class='px-2 py-4'>
    {#if active == 'deskripsi'}
        <slot name='deskripsi' />
    {:else}
        <slot name='ulasan' />
    {/if}
</div>