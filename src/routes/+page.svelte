<script lang="ts">
    import ProductCard from "$lib/ProductCard.svelte";

    const produk = ['Tirai Kantor', 'Gorden', 'Roller Blind', 'Wallpaper Dinding']
    const products = Array(16)
</script>

<div class="h-screen flex relative justify-center px-20 flex-col bg-orange-100">
    <div class='w-2/3'>
        <h6 class="mb-5 text-lg font-medium">Jual {produk.join(', ')}</h6>
        <h1 class="text-5xl font-bold mb-8 text-orange-600 uppercase">Margon Interior</h1>
        <p class="leading-relaxed">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo sit ipsum in. Asperiores autem numquam, hic deleniti molestias repellat laudantium consectetur harum exercitationem ipsa. Dolorum odio provident velit sapiente suscipit?</p>
        
        <div class="flex gap-2 mt-8">
            <a class="px-3 py-2 border border-orange-500 rounded-sm text-orange-500 duration-200 hover:bg-orange-500 hover:text-white" href="/produk">Lihat Produk</a>
            <a class="px-3 py-2 border border-orange-500 rounded-sm text-orange-500 duration-200 hover:bg-orange-500 hover:text-white" href="/profil">Tentang Kami</a>
        </div>
    </div>

    <div class="items-center grid grid-cols-3 absolute bottom-0 translate-y-1/2 w-2/3 left-1/2 -translate-x-1/2 h-40 bg-white">
        <div class="h-full bg-stone-200 flex items-center">
            <span class="font-semibold w-full text-2xl text-center">Produk Berkualitas</span>
        </div>
        <div class="h-full bg-stone-300 flex items-center">
            <span class="font-semibold w-full text-2xl text-center">Layanan Bergaransi</span>
        </div>
        <div class="h-full bg-stone-200 flex items-center">
            <span class="font-semibold w-full text-2xl text-center">Pilihan Terlengkap</span>
        </div>
    </div>
</div>

<div class="mt-44 mb-16">
    <div class="w-5/6 mx-auto">
        <div class="text-center">
            <h6 class='text-xl font-medium mb-2'>Produk Terbaru</h6>
            <h2 class="text-5xl font-bold mb-8">Margon Interior</h2>
            <p class="font-medium text-lg w-1/3 mx-auto">Jual Tirai Kantor, Gorden, Stiker Kaca, Roller Blind, Wallpaper Dinding Makassar</p>
            <div class="h-1 w-1/12 bg-orange-500 mx-auto mt-5">&nbsp;</div>
        </div>

        <div class="grid grid-cols-4 gap-3 mt-14">
            {#each products as v,i}
                <ProductCard product_id={i + 1} product_name="Contoh Product {i + 1}" price={25000 * (i + 1.8)} />
            {/each}
        </div>
    </div>
</div>

<div class="bg-orange-500 pt-10 pb-24 text-white flex justify-center flex-col">
    <div class="w-11/12 mx-auto">
        <h2 class="font-bold text-4xl mb-5">Margon Interior</h2>
        <p class="w-2/3 leading-relaxed">Distributor dan penjualan produk-produk kebutuhan interior terbaik di Makassar, Sulawesi Selatan. Menyediakan berbagai produk seperti window blind, tirai kantor, gorden, stiker kaca, roller blind, dan wallpaper dinding berkualitas terbaik dengan harga yang kompetitif.</p>
    </div>
</div>

<div class="w-11/12 ml-auto -mt-12">
    <div class="w-3/4 ml-auto bg-white py-12 px-14 flex relative">
        <div class="w-1/4">
            <img src="https://cdn.margoninterior.com/2023/05/profil-margon-interior.jpg" alt="contoh" class="absolute top-1/4 -translate-y-1/4 left-8 -translate-x-2/3 w-3/5">
        </div>

        <div class="w-3/4">
            <h2 class="text-4xl mb-6 font-semibold">Tentang Kami</h2>
            <p class="leading-relaxed mb-4"><strong>Margon Interior</strong> merupakan perusahaan yang bergerak di bidang distributor produk-produk interior berupa window blind dan aksesoris interior lainnya yang berlokasi di Makassar. Produk yang kami sediakan dan kami jual yaitu seperti <strong>roller blind, horizontal blind, vertical blind, venetian blind, wooden blind, tirai kantor, gorden, dan wallpaper dinding.</strong></p>
            <p class="leading-relaxed mb-8">Selain menyediakan dan menjual berbagai produk window blind, kami juga menyediakan layanan pemasangan bergaransi untuk produk window blind yang kami jual.</p>
            <a href="/profil" class="border-orange-500 px-3 py-2 text-orange-500 border block w-fit duration-200 hover:bg-orange-500 hover:text-white">Baca Selengkapnya</a>
        </div>
    </div>
</div>