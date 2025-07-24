<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';

  let isMounted = false;

  onMount(() => {
    isMounted = true;
    return () => {};
  });
</script>

<svelte:head>
  <title>vrl website</title>
</svelte:head>

<div class="min-h-screen bg-green-50">
  <!-- Hero Section -->
  <section id="home" class="py-8 sm:py-12 md:py-16 text-center">
    <div class="container mx-auto px-4">
      {#if isMounted}
        <div transition:fade={{ duration: 500 }}>
          <h1 class="text-xl sm:text-2xl md:text-3xl lg:text-4xl font-bold text-blue-800 mb-2">Selamat Datang di vrl website</h1>
          <p class="text-base sm:text-lg md:text-xl text-gray-700 mb-4">VPS Terbaik untuk anda</p>
          <a href="#products" class="inline-block bg-blue-600 text-white py-1 px-3 sm:py-2 sm:px-4 md:py-2 md:px-6 rounded hover:bg-blue-700 transition">Lihat Produk</a>
        </div>
      {/if}
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="py-8 sm:py-12 md:py-16 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-xl sm:text-2xl md:text-3xl font-bold text-blue-800 text-center mb-6 sm:mb-8">Produk Kami</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 sm:gap-6">
        <div class="bg-white p-3 sm:p-4 rounded-lg shadow-md border border-gray-200 text-center max-w-xs mx-auto">
          <div class="flex justify-center mb-2 sm:mb-4">
            <img src="https://via.placeholder.com/40" alt="Baremetal Icon" class="w-8 h-8 sm:w-12 h-12" />
          </div>
          <h3 class="text-base sm:text-lg font-semibold text-gray-800 mb-2">Deploy Baremetal Server</h3>
          <p class="text-gray-600 mb-2 sm:mb-4 text-sm sm:text-base">Dedicated physical servers with full root access</p>
          <ul class="text-gray-600 text-center space-y-1 sm:space-y-2 mb-2 sm:mb-4">
            <li>⚡ High-Performance Hardware</li>
            <li>🔒 Isolated Environments</li>
            <li>📊 Resource Monitoring</li>
          </ul>
          <a href="https://wa.me/628510523609?text=Saya%20tertarik%20dengan%20Deploy%20Baremetal%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-1 px-2 sm:py-2 sm:px-4 rounded hover:bg-yellow-500 transition text-sm sm:text-base">Deploy Server</a>
        </div>
        <div class="bg-white p-3 sm:p-4 rounded-lg shadow-md border border-gray-200 text-center max-w-xs mx-auto">
          <div class="flex justify-center mb-2 sm:mb-4">
            <img src="https://via.placeholder.com/40" alt="Custom Server Icon" class="w-8 h-8 sm:w-12 h-12" />
          </div>
          <h3 class="text-base sm:text-lg font-semibold text-gray-800 mb-2">Buy Custom Server</h3>
          <p class="text-gray-600 mb-2 sm:mb-4 text-sm sm:text-base">Tailor-made server solutions for enterprise needs</p>
          <ul class="text-gray-600 text-center space-y-1 sm:space-y-2 mb-2 sm:mb-4">
            <li>🔧 Custom Hardware Configuration</li>
            <li>📦 Bulk Order Management</li>
            <li>🌐 Global Distribution Network</li>
          </ul>
          <a href="https://wa.me/6285710523609?text=Saya%20tertarik%20dengan%20Buy%20Custom%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-1 px-2 sm:py-2 sm:px-4 rounded hover:bg-yellow-500 transition text-sm sm:text-base">Buy Server</a>
        </div>
        <div class="bg-white p-3 sm:p-4 rounded-lg shadow-md border border-gray-200 text-center max-w-xs mx-auto">
          <div class="flex justify-center mb-2 sm:mb-4">
            <img src="https://via.placeholder.com/40" alt="VPS Icon" class="w-8 h-8 sm:w-12 h-12" />
          </div>
          <h3 class="text-base sm:text-lg font-semibold text-gray-800 mb-2">Virtual Private Server</h3>
          <p class="text-gray-600 mb-2 sm:mb-4 text-sm sm:text-base">Flexible virtual machine instances</p>
          <ul class="text-gray-600 text-center space-y-1 sm:space-y-2 mb-2 sm:mb-4">
            <li>💾 SSD Storage</li>
            <li>🌐 Dedicated IP</li>
            <li>📸 Snapshot Backups</li>
          </ul>
          <a href="https://wa.me/6285710523609?text=Saya%20tertarik%20dengan%20Virtual%20Private%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-1 px-2 sm:py-2 sm:px-4 rounded hover:bg-yellow-500 transition text-sm sm:text-base">Get Started</a>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-8 sm:py-12 md:py-16 bg-green-50">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-xl sm:text-2xl md:text-3xl font-bold text-blue-800 mb-4">Tentang Kami</h2>
      <p class="text-gray-700 max-w-xs sm:max-w-md md:max-w-lg mx-auto mb-4">vrl website adalah penyedia layanan vps terbaik untuk anda.</p>
      <a href="#contact" class="inline-block bg-blue-600 text-white py-1 px-3 sm:py-2 sm:px-4 md:py-2 md:px-6 rounded hover:bg-blue-700 transition">Hubungi Kami</a>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-8 sm:py-12 md:py-16 bg-green-50">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-xl sm:text-2xl md:text-3xl font-bold text-blue-800 mb-4">Hubungi Kami</h2>
      <a href="https://wa.me/6285710523609" target="_blank" class="inline-block bg-green-600 text-white py-1 px-3 sm:py-2 sm:px-4 md:py-2 md:px-6 rounded hover:bg-green-700 transition">Chat via WhatsApp</a>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-blue-600 text-white py-2 sm:py-4">
    <div class="container mx-auto px-4 text-center">
      <p class="text-xs sm:text-sm">© 2025 vrl website. All rights reserved.</p>
      <p class="mt-1 text-xs sm:text-sm">Email: plitvicegod@gmail.com</p>
    </div>
  </footer>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

  :global(body) {
    font-family: 'Poppins', sans-serif;
  }
</style>