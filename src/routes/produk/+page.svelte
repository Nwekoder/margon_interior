<script lang="ts">
    import ProductCard from "$lib/ProductCard.svelte";

    const products = Array(16)
</script>

<div class="mt-12 mb-16">
    <div class="w-11/12 mx-auto">
        <div class="text-center">
            <h2 class="text-5xl font-bold mb-5">Produk</h2>
            <div class="h-1 w-1/12 bg-orange-500 mx-auto mt-1">&nbsp;</div>
        </div>

        <div class="grid grid-cols-10 mt-12 gap-2">
            <div class="col-span-2">
                hello
            </div>

            <div class="col-span-8 grid grid-cols-4 gap-2">
                {#each products as v,i}
                    <ProductCard product_id={i + 1} product_name="Contoh Product {i + 1}" price={25000 * (i + 1.8)} />
                {/each}
            </div>
        </div>
    </div>
</div>