<script lang="ts">
    import '../app.css'
	import Navbar from '$lib/Navbar.svelte';    
</script>

<Navbar />

<div class="pt-20 min-h-screen">
    <slot />
</div>

<footer class="bg-stone-800 text-white min-h-[40vh] flex items-center pt-16 pb-5">
    <div class="w-5/6 mx-auto">
        <div class="grid grid-cols-6 gap-2">
            <div class="col-span-2">
                <h3 class="text-2xl font-bold mb-5">Margon Interior</h3>
                <p class="leading-relaxed">Solusi tepat untuk kebutuhan berbagai produk window blind berkualitas dengan harga termurah di Sulawesi. Silakan hubungi kami untuk mendapatkan produk window blind terbaik.</p>
            </div>
    
            <!-- Categories -->
            <div>
    
            </div>
    
            <!-- Contact Number -->
            <div>
    
            </div>
    
            <!-- Statistics -->
            <div>
    
            </div>
        </div>
    
        <div class="w-full opacity-30 mx-auto h-0.5 my-4 bg-white">&nbsp;</div>

        <div class="w-full mx-auto text-center text-sm text-stone-400">
            ©2023 Margon Interior. All Rights Reserved.
        </div>
    </div>
</footer>