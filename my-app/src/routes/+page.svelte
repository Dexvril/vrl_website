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

<div class="min-h-screen bg-gradient-to-b from-blue-100 to-green-100">
  <!-- Navbar -->
  <nav class="bg-blue-600 text-white p-4 sticky top-0 shadow-md">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold">vrl website</h1>
      <ul class="flex space-x-6">
        <li><a href="#home" class="hover:text-green-200">Beranda</a></li>
        <li><a href="#products" class="hover:text-green-200">Produk</a></li>
        <li><a href="#about" class="hover:text-green-200">Tentang</a></li>
        <li><a href="#contact" class="hover:text-green-200">Kontak</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="py-20 text-center bg-green-50">
    <div class="container mx-auto px-4">
      {#if isMounted}
        <div transition:fade={{ duration: 500 }}>
          <h2 class="text-4xl md:text-5xl font-bold text-blue-800 mb-4">
            Selamat Datang di vrl website
          </h2>
          <p class="text-lg md:text-xl text-gray-700 mb-6">
            VPS Terbaik untuk anda
          </p>
          <a
            href="#products"
            class="inline-block bg-green-600 text-white py-3 px-6 rounded-lg hover:bg-green-700 transition"
          >
            Lihat Produk
          </a>
        </div>
      {/if}
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-blue-800 text-center mb-12">Produk Kami</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200">
          <div class="flex justify-center mb-4">
            <img src="https://via.placeholder.com/50" alt="Baremetal Icon" class="w-12 h-12" />
          </div>
          <h3 class="text-xl font-semibold text-gray-800 text-center mb-2">Deploy Baremetal Server</h3>
          <p class="text-gray-600 text-center mb-4">Dedicated physical servers with full root access</p>
          <ul class="text-gray-600 text-center space-y-2 mb-4">
            <li>⚡ High-Performance Hardware</li>
            <li>🔒 Isolated Environments</li>
            <li>📊 Resource Monitoring</li>
          </ul>
          <a href="https://wa.me/6285710523609?text=Saya%20tertarik%20dengan%20Deploy%20Baremetal%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-2 px-4 rounded text-center hover:bg-yellow-500 transition">Deploy Server</a>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200">
          <div class="flex justify-center mb-4">
            <img src="https://via.placeholder.com/50" alt="Custom Server Icon" class="w-12 h-12" />
          </div>
          <h3 class="text-xl font-semibold text-gray-800 text-center mb-2">Buy Custom Server</h3>
          <p class="text-gray-600 text-center mb-4">Tailor-made server solutions for enterprise needs</p>
          <ul class="text-gray-600 text-center space-y-2 mb-4">
            <li>🔧 Custom Hardware Configuration</li>
            <li>📦 Bulk Order Management</li>
            <li>🌐 Global Distribution Network</li>
          </ul>
          <a href="https://wa.me/6285710523609?text=Saya%20tertarik%20dengan%20Buy%20Custom%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-2 px-4 rounded text-center hover:bg-yellow-500 transition">Buy Server</a>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200">
          <div class="flex justify-center mb-4">
            <img src="https://via.placeholder.com/50" alt="VPS Icon" class="w-12 h-12" />
          </div>
          <h3 class="text-xl font-semibold text-gray-800 text-center mb-2">Virtual Private Server</h3>
          <p class="text-gray-600 text-center mb-4">Flexible virtual machine instances</p>
          <ul class="text-gray-600 text-center space-y-2 mb-4">
            <li>💾 SSD Storage</li>
            <li>🌐 Dedicated IP</li>
            <li>📸 Snapshot Backups</li>
          </ul>
          <a href="https://wa.me/6285710523609?text=Saya%20tertarik%20dengan%20Virtual%20Private%20Server%20anda" target="_blank" class="block bg-yellow-400 text-black font-bold py-2 px-4 rounded text-center hover:bg-yellow-500 transition">Get Started</a>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16 bg-blue-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-blue-800 text-center mb-12">Tentang Kami</h2>
      <p class="text-gray-700 text-center max-w-2xl mx-auto">
        vrl website adalah penyedia layanan terbaik untuk anda.
      </p>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-16 bg-green-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-blue-800 text-center mb-12">Hubungi Kami</h2>
      <div class="max-w-lg mx-auto text-center">
        <a
          href="https://wa.me/6285710523609"
          target="_blank"
          class="inline-block bg-green-600 text-white py-3 px-6 rounded-lg hover:bg-green-700 transition"
        >
          Chat via WhatsApp
        </a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-blue-600 text-white py-6">
    <div class="container mx-auto px-4 text-center">
      <p>© 2025 vrl website. All rights reserved.</p>
      <p class="mt-2">Email: plitvicegod@gmail.com</p>
    </div>
  </footer>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

  :global(body) {
    font-family: 'Poppins', sans-serif;
  }
</style>