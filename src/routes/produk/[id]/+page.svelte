<script lang="ts">
    import Breadcrumb from "$lib/Breadcrumb.svelte";
    import {page} from '$app/stores'
	import Tab from "$lib/Tab.svelte";
</script>

<div class="w-11/12 mx-auto py-4 grid grid-cols-12 gap-2">
    <div class="col-span-9">
        <Breadcrumb path={$page.url.pathname.split('/')} />

        <div class="grid grid-cols-5 gap-2 mt-4">
            <div class="col-span-2">
                <img src="https://www.margoninterior.com/wp-content/uploads/2023/05/roller-blind-shinichi.jpg" alt="Gambar">
            </div>
            <div class="col-span-3 px-5">
                <h1 class="text-3xl font-bold mb-6">Contoh Barang {$page.params.id}</h1>
                <p class="text-justify mb-6">Cari Roller Blind Murah di Makassar? Kami menjual juga melayani pasang Roller Blind merek Shinichi untuk di kantor, mall, rumah, rukan, di wilayah Makassar dan beberapa kota lain. Roller blind merupakan suatu tirai gulung dari bawah keatas secara chain system atau spring system yang amat lentur melengkapi dekorasi dan keindahan bermacam-macam tipe ruangan. Dengan fabric alternatif roller blind jadi solusi untuk mereduksi dampak negatif cahaya panas matahari. Roller blind adalah window fashion amat cocok diaplikasikan di gedung perkantoran, apartemen, restauran, rumah dan area publik.</p>
                <a href="/" class="px-3 py-2 bg-orange-500 block w-fit text-white duration-200 hover:bg-orange-600">Beli Sekarang</a>
            </div>
        </div>

        <Tab>
            <div slot='deskripsi'>
                <p class="leading-relaxed text-justify">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quia nulla beatae illo est consequatur officiis consectetur repellat, qui accusantium dolorum numquam. Repellat nulla deleniti eos, explicabo dolor ipsam recusandae quibusdam! Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cumque id libero iure vel ut distinctio autem magni vitae facere aut nobis itaque repellat hic incidunt inventore quisquam minima, accusamus nostrum. Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam, veritatis nisi quas illum aliquid laudantium. Eligendi reprehenderit aperiam cupiditate totam blanditiis eum, incidunt eos labore. Voluptatibus facere aut ipsam numquam.</p>
            </div>
            <div slot='ulasan'>
                <h2>Hei</h2>
            </div>
        </Tab>
    </div>

    <div class="col-span-3">
        hei
    </div>
</div>