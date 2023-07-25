<script lang="ts">
    export let product_id:number;
    export let product_name:string;
    export let price:number;

    const priceFormat = Intl.NumberFormat('id', {currency: 'IDR'}).format(price)
</script>

<div class="w-full relative bg-gray-200 px-3 py-2 rounded-md overflow-hidden">
    <div class="p-2">
        <img class="w-full aspect-square rounded-lg" src="https://www.margoninterior.com/wp-content/uploads/2023/05/roller-blind-onna-300x300.jpg" alt="contoh 1">
    </div>

    <div class="py-4 pt-10">
        <h5 class="text-lg">{product_name}</h5>
        <p class="text-sm">Variant: 1</p>
    </div>

    <span class="absolute right-0 top-1/2 min-w-[45%] text-right text-white font-medium rounded-l-sm -translate-y-1/2 px-4 py-2 bg-orange-600 text-sm">Mulai dari<br/>Rp. {priceFormat}</span>

    <div class="grid grid-cols-2 gap-1">
        <a class="bg-cyan-600 duration-200 hover:bg-cyan-800 px-2 py-3 rounded-sm text-center text-white" href="/produk/{product_id}">Info</a>
        <a class="bg-green-500 duration-200 hover:bg-green-700 px-2 py-3 rounded-sm text-center text-white" href="/">Beli Sekarang</a>
    </div>
</div>