<script lang="ts">
	const namaPria = 'ANDI';
	const namaWanita = 'SITI';
	const tanggal = '2025-08-17T10:00:00';
	const lokasi = 'https://maps.google.com/?q=Masjid+Agung+Binjai';
</script>

<!-- Navbar -->
<nav class="fixed top-0 left-0 z-10 w-full bg-white shadow-md">
	<div class="mx-auto flex max-w-5xl items-center justify-between px-4 py-3">
		<span class="text-xl font-bold text-purple-600">{namaPria} ❤️ {namaWanita}</span>
		<ul class="flex gap-4 text-sm text-gray-600">
			<li><a href="#beranda" class="hover:text-purple-700">Beranda</a></li>
			<li><a href="#lokasi" class="hover:text-purple-700">Lokasi</a></li>
			<li><a href="#ucapan" class="hover:text-purple-700">Ucapan</a></li>
		</ul>
	</div>
</nav>

<!-- Hero Section -->
<section
	id="beranda"
	class="flex min-h-screen flex-col items-center justify-center bg-gradient-to-br from-pink-200 to-purple-300 px-6 pt-24 md:flex-row-reverse"
>
	<!-- Gambar -->
	<div class="pb-6 md:w-auto">
		<img
			src="image/pernikahan.png"
			alt="Muhammad Gifary"
			class="w-full max-w-lg rounded-full bg-purple-500 object-cover px-4 shadow-xl transition duration-300 ease-in-out hover:scale-105 md:w-[350px] md:rounded-none md:rounded-r-full"
		/>
	</div>

	<!-- Teks -->
	<div class="text-center md:text-left">
		<h1 class="mb-4 text-4xl font-bold text-pink-700">Undangan Pernikahan</h1>
		<p class="mb-2 text-lg text-gray-800">
			Kami mengundang Anda untuk hadir dalam acara pernikahan kami
		</p>
		<h2 class="mt-4 text-3xl font-semibold text-purple-800">{namaPria} &amp; {namaWanita}</h2>
	</div>
</section>

<!-- Lokasi -->
<section id="lokasi" class="bg-white px-4 py-16">
	<h2 class="mb-4 text-center text-2xl font-bold text-purple-700">Lokasi Acara</h2>
	<div class="mx-auto aspect-video max-w-3xl overflow-hidden rounded-xl shadow-lg">
		<iframe
			title="Lokasi Acara"
			src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3982.1627000137176!2d98.47314717593346!3d3.620221696382897!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3031311e2db37b4b%3A0x8a5a6e4d81b5f2f4!2sJl.%20Sisingamangaraja%20No.42%2C%20Nangka%2C%20Kec.%20Binjai%20Utara%2C%20Kota%20Binjai%2C%20Sumatera%20Utara!5e0!3m2!1sen!2sid!4v1717054190000!5m2!1sen!2sid"
			class="h-full w-full border-4 border-purple-400"
			allowfullscreen
			loading="lazy"
			referrerpolicy="no-referrer-when-downgrade"
		></iframe>
	</div>
</section>

<section class="mt-10 bg-purple-200 px-4 py-16 text-center">
	<h3 class="mb-6 text-2xl font-bold text-purple-800">Kenangan Kami</h3>

	<div class="mx-auto grid max-w-4xl grid-cols-2 justify-items-center gap-4 md:grid-cols-4">
		<img
			src="https://picsum.photos/id/1015/400/300"
			alt="Kenangan 1"
			class="rounded-lg shadow-md transition duration-300 ease-in-out hover:scale-105 hover:rotate-1 hover:shadow-2xl"
		/>
		<img
			src="https://picsum.photos/id/1016/400/300"
			alt="Kenangan 2"
			class="rounded-lg shadow-md transition duration-300 ease-in-out hover:scale-105 hover:rotate-1 hover:shadow-2xl"
		/>
		<img
			src="https://picsum.photos/id/1018/400/300"
			alt="Kenangan 3"
			class="rounded-lg shadow-md transition duration-300 ease-in-out hover:scale-105 hover:rotate-1 hover:shadow-2xl"
		/>
		<img
			src="https://picsum.photos/id/1019/400/300"
			alt="Kenangan 3"
			class="rounded-lg shadow-md transition duration-300 ease-in-out hover:scale-105 hover:rotate-1 hover:shadow-2xl"
		/>
	</div>

	<div class="mt-8">
		<a
			href="/kenangan"
			class="inline-block rounded-full bg-purple-600 px-6 py-3 text-white shadow-md transition hover:scale-105 hover:bg-purple-800"
		>
			Lihat Kenangan Kami Lainnya
		</a>
	</div>
</section>
<section class="bg-white py-10 text-center">
	<h3 class="mb-4 text-xl font-bold text-purple-700">Konfirmasi Kehadiran</h3>
	<a
		href="https://wa.me/6281234567890?text=Halo,%20Saya%20akan%20hadir%20di%20acara%20pernikahan%20{namaPria}%20dan%20{namaWanita}"
		target="_blank"
		class="inline-block rounded-lg bg-purple-600 px-6 py-3 text-white shadow-md transition hover:bg-purple-800"
	>
		Konfirmasi via WhatsApp
	</a>
</section>

<!-- Ucapan Section -->
<section
	id="ucapan"
	class="rounded-t-full border-4 border-purple-700 bg-purple-200 px-4 pt-16 pb-10 text-center text-white"
>
	<h3 class="mb-4 text-xl font-semibold text-purple-800">Ucapan & Doa</h3>
	<p class="mx-auto max-w-xl text-sm text-gray-800">
		Semoga pernikahan ini menjadi awal dari kehidupan yang penuh berkah, kebahagiaan, dan cinta yang
		abadi.
	</p>
</section>

<!-- Footer -->
<footer id="footer" class="bg-purple-700 py-6 text-center text-white">
	<p class="mb-4 text-sm">© 2025 Muhammad Andi & Siti Aisyah</p>
	<div class="flex justify-center space-x-4">
		<a href="https://instagram.com/gif_ry02" target="_blank" aria-label="Instagram">
			<svg
				class="h-6 w-6 fill-white transition hover:fill-pink-400"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 24 24"
			>
				<path
					d="M12 2.2c3.2 0 3.6 0 4.9.1 1.2.1 1.9.3 2.3.5.6.3 1.1.7 1.5 1.3.4.5.7 1.2.8 2.3.1 1.3.1 1.7.1 4.9s0 3.6-.1 4.9c-.1 1.2-.3 1.9-.5 2.3-.3.6-.7 1.1-1.3 1.5-.5.4-1.2.7-2.3.8-1.3.1-1.7.1-4.9.1s-3.6 0-4.9-.1c-1.2-.1-1.9-.3-2.3-.5-.6-.3-1.1-.7-1.5-1.3-.4-.5-.7-1.2-.8-2.3C2.2 15.6 2.2 15.2 2.2 12s0-3.6.1-4.9c.1-1.2.3-1.9.5-2.3.3-.6.7-1.1 1.3-1.5.5-.4 1.2-.7 2.3-.8C8.4 2.2 8.8 2.2 12 2.2m0-2.2C8.7 0 8.3 0 7 .1 5.7.1 4.8.3 4.1.6c-.8.3-1.5.8-2.2 1.5C1.1 3.1.6 3.9.3 4.7.1 5.4 0 6.3 0 7.6 0 8.9 0 9.3 0 12s0 3.1.1 4.4c.1 1.3.3 2.2.6 2.9.3.8.8 1.5 1.5 2.2.7.7 1.4 1.2 2.2 1.5.7.3 1.6.5 2.9.6C8.7 24 9.1 24 12 24s3.1 0 4.4-.1c1.3-.1 2.2-.3 2.9-.6.8-.3 1.5-.8 2.2-1.5.7-.7 1.2-1.4 1.5-2.2.3-.7.5-1.6.6-2.9.1-1.3.1-1.7.1-4.4s0-3.1-.1-4.4c-.1-1.3-.3-2.2-.6-2.9-.3-.8-.8-1.5-1.5-2.2-.7-.7-1.4-1.2-2.2-1.5-.7-.3-1.6-.5-2.9-.6C15.3 0 14.9 0 12 0zm0 5.8a6.2 6.2 0 1 0 0 12.4 6.2 6.2 0 0 0 0-12.4zm0 10.2a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.4-11.6a1.4 1.4 0 1 0 0 2.8 1.4 1.4 0 0 0 0-2.8z"
				/>
			</svg>
		</a>
		<a href="https://wa.me/6281234567890" target="_blank" aria-label="WhatsApp">
			<svg
				class="h-6 w-6 fill-white transition hover:fill-green-400"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 32 32"
			>
				<path
					d="M16 .1C7.3.1.1 7.3.1 16c0 2.8.7 5.4 2 7.8L0 32l8.5-2.2a15.9 15.9 0 0 0 7.5 1.9c8.7 0 15.9-7.2 15.9-15.9S24.7.1 16 .1zm0 29.1c-2.4 0-4.7-.6-6.7-1.7l-.5-.3-5 1.3 1.3-4.8-.3-.5a13.2 13.2 0 0 1-2-7c0-7.3 6-13.3 13.3-13.3s13.3 6 13.3 13.3-6 13.3-13.3 13.3zm7.2-9.9c-.4-.2-2.2-1.1-2.5-1.3-.3-.1-.6-.2-.8.2-.3.4-.9 1.3-1.1 1.5-.2.2-.4.3-.8.1a10.7 10.7 0 0 1-3.1-1.9 11.6 11.6 0 0 1-2.2-2.8c-.2-.4 0-.6.2-.8l.5-.6c.2-.2.2-.4.3-.6.1-.3 0-.5 0-.7-.1-.2-.8-2-1.1-2.7-.3-.6-.5-.6-.8-.6l-.7-.1c-.2 0-.5 0-.8.4-.3.4-1 1-1 2.5 0 1.5 1 3 1.2 3.2.2.3 2 3.2 4.8 4.5 2.8 1.2 2.8.8 3.3.8.5 0 1.6-.7 1.8-1.4.2-.6.2-1.3.2-1.4 0-.2-.2-.2-.4-.3z"
				/>
			</svg>
		</a>
	</div>
</footer>
