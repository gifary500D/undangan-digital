<script lang="ts">
	import { fade, fly } from 'svelte/transition';

	const namaPria = 'ANDI';
	const namaWanita = 'SITI';
	const tanggal = '2025-08-17T10:00:00';
	const lokasi = 'https://maps.google.com/?q=Masjid+Agung+Binjai';

	import { onMount } from 'svelte';

	let timerEl: HTMLParagraphElement | null = null;

	onMount(() => {
		function updateTimer() {
			if (!timerEl) return;

			const now = new Date();
			const targetDate = new Date('2025-08-01T00:00:00');
			const diff = targetDate.getTime() - now.getTime();

			if (diff > 0) {
				const days = Math.floor(diff / (1000 * 60 * 60 * 24));
				const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
				const minutes = Math.floor((diff / (1000 * 60)) % 60);
				const seconds = Math.floor((diff / 1000) % 60);

				timerEl.textContent = `${days} hari ${hours} jam ${minutes} menit ${seconds} detik`;
			} else {
				timerEl.textContent = 'Waktu telah habis!';
			}
		}

		const interval = setInterval(updateTimer, 1000);
		updateTimer(); // panggilan pertama

		return () => clearInterval(interval); // bersihkan saat komponen dibuang
	});
</script>

<svelte:head>
	<link href="https://fonts.googleapis.com/css2?family=Alex+Brush&display=swap" rel="stylesheet" />

	<link href="https://fonts.googleapis.com/css2?family=Alex+Brush&display=swap" rel="stylesheet" />
	<style>
		:root {
			--font-heading: 'Great Vibes', cursive;
			--font-body: 'Poppins', sans-serif;
		}
		html {
			scroll-behavior: smooth;
		}
	</style>
</svelte:head>
<!-- Navbar -->
<nav class="fixed top-0 left-0 z-10 w-full bg-white shadow-md dark:bg-gray-900">
	<div class="mx-auto flex max-w-5xl items-center justify-between px-4 py-3">
		<span
			style="font-family: var(--font-heading)"
			class="text-xl font-bold text-purple-600 dark:text-purple-400"
			>{namaPria} ❤️ {namaWanita}</span
		>
		<ul class="text-md flex gap-4 font-semibold text-teal-600 dark:text-teal-400">
			<li>
				<a href="#beranda" class="hover:text-purple-700 dark:hover:text-purple-300">Beranda</a>
			</li>
			<li><a href="#lokasi" class="hover:text-purple-700 dark:hover:text-purple-300">Lokasi</a></li>
			<li><a href="#ucapan" class="hover:text-purple-700 dark:hover:text-purple-300">Ucapan</a></li>
		</ul>
	</div>
</nav>

<section
	id="beranda"
	class="relative flex min-h-screen flex-col items-center justify-center overflow-hidden bg-gradient-to-br from-pink-200 to-purple-300 px-6 pt-24 md:flex-row-reverse dark:from-purple-900 dark:to-pink-900"
>
	<!-- Background image di belakang -->
	<div
		class="absolute inset-0 z-0 bg-[url('image/bg-nikah.jpg')] bg-cover bg-center opacity-20 dark:opacity-5"
	></div>

	<!-- Kontainer konten utama -->
	<div class="relative flex w-full flex-col items-center justify-center md:flex-row-reverse">
		<!-- Gambar -->
		<div class="pb-6 md:pb-0 md:pl-6">
			<img
				src="image/pernikahan.png"
				alt="Pernikahan"
				class="w-full max-w-xs rounded-full bg-purple-500 object-cover shadow-xl transition duration-300 ease-in-out hover:scale-105 md:max-w-sm md:rounded-none md:rounded-r-full dark:bg-purple-700"
			/>
		</div>

		<!-- Teks -->
		<div class="text-center md:pr-6 md:text-left">
			<h1 class="mb-4 text-4xl font-bold text-pink-700 dark:text-pink-300">Undangan Pernikahan</h1>
			<p
				style="font-family: 'Playfair Display', serif;"
				class="mb-2 text-lg text-gray-800 dark:text-gray-200"
			>
				Kami mengundang Anda untuk hadir dalam acara pernikahan kami
			</p>
			<h2
				style="font-family: 'Playfair Display', serif;"
				class="mt-4 pb-4 text-3xl font-semibold text-purple-800 dark:text-purple-200"
			>
				{namaPria} &amp; {namaWanita}
			</h2>
		</div>
	</div>
</section>

<!-- Kutipan Section -->
<section class="bg-white px-4 py-24 text-center dark:bg-gray-800">
	<blockquote class="mx-auto max-w-2xl text-lg text-gray-700 italic dark:text-gray-300">
		" <span class="text-2xl font-semibold text-pink-700 dark:text-pink-300">Cinta</span> tidak
		menciptakan pernikahan. Pernikahan yang sadar, terencana, menciptakan
		<span class="text-2xl font-semibold text-pink-700 dark:text-pink-300">Cinta</span>. Hal yang
		sama terjadi dalam semua hubungan. " <br />
		<span class="mt-2 block font-semibold text-purple-700 dark:text-purple-300"
			>- Harville Hendrix</span
		>
	</blockquote>
	<!--Kenangan section-->
</section>
<section class="mt-10 bg-purple-200 px-4 py-16 text-center dark:bg-purple-800">
	<h3 class="mb-6 text-4xl font-bold text-purple-800 dark:text-purple-200">Kenangan Kami</h3>

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
			src="https://picsum.photos/id/1014/400/300"
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
			class="active-scale-95 inline-block rounded-lg bg-purple-600 px-6 py-3 text-white shadow-md transition hover:scale-105 hover:bg-purple-800 dark:bg-purple-700 dark:hover:bg-purple-600"
		>
			Lihat Kenangan Kami Lainnya
		</a>
	</div>
</section>
<!-- Lokasi -->
<section id="lokasi" class="bg-white px-4 py-16 dark:bg-gray-800">
	<h2 class="mb-4 text-center text-4xl font-bold text-purple-700 dark:text-purple-300">
		Lokasi Acara
	</h2>
	<div
		class=" hover:shadow-2x mx-auto aspect-video max-w-3xl overflow-hidden rounded-xl shadow-lg transition duration-300 ease-in-out hover:scale-105"
	>
		<iframe
			title="Lokasi Acara"
			src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3982.1627000137176!2d98.47314717593346!3d3.620221696382897!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3031311e2db37b4b%3A0x8a5a6e4d81b5f2f4!2sJl.%20Sisingamangaraja%20No.42%2C%20Nangka%2C%20Kec.%20Binjai%20Utara%2C%20Kota%20Binjai%2C%20Sumatera%20Utara!5e0!3m2!1sen!2sid!4v1717054190000!5m2!1sen!2sid"
			class="h-full w-full border-4 border-purple-400 dark:border-purple-500"
			allowfullscreen
			loading="lazy"
			referrerpolicy="no-referrer-when-downgrade"
		></iframe>
	</div>
</section>

<!-- cerita -->
<section
	class="bg-gradient-to-r from-purple-100 to-pink-100 px-4 py-12 dark:from-purple-900 dark:to-pink-900"
>
	<div class="mx-auto max-w-4xl text-center">
		<h3 class="mb-8 text-2xl font-bold text-purple-800 dark:text-purple-200">
			Cerita Cinta <span class="text-xl text-pink-600 dark:text-pink-300">Kami</span>
		</h3>

		<div class="rounded-lg bg-white p-8 shadow-lg dark:bg-gray-800">
			<p class="mb-4 leading-relaxed text-gray-700 dark:text-gray-300">
				"Pertemuan pertama <span class="text-xl text-pink-600 dark:text-pink-300">kami</span> adalah
				kebetulan yang indah. Siapa sangka bahwa dua orang yang berbeda latar belakang bisa saling melengkapi
				dengan sempurna."
			</p>
			<p class="mb-4 leading-relaxed text-gray-700 dark:text-gray-300">
				"Dari teman biasa, menjadi sahabat, kemudian berkembang menjadi cinta yang mendalam. Setiap
				hari bersama terasa seperti petualangan baru bagi <span
					class="text-xl text-pink-600 dark:text-pink-300">kami</span
				>."
			</p>
			<p class="leading-relaxed text-gray-700 dark:text-gray-300">
				"<span class="text-xl text-pink-600 dark:text-pink-300">Kami</span> percaya bahwa cinta
				sejati adalah tentang saling mendukung, menghargai, dan tumbuh bersama. Inilah fondasi yang
				akan
				<span class="text-xl text-pink-600 dark:text-pink-300">kami</span>
				bawa ke dalam pernikahan
				<span class="text-xl text-pink-600 dark:text-pink-300">kami</span>."
			</p>
		</div>
	</div>
</section>
<!-- Konfirmasi -->
<section class="bg-white py-10 text-center dark:bg-gray-800">
	<h3 class="mb-4 text-xl font-bold text-purple-700 dark:text-purple-300">Konfirmasi Kehadiran</h3>
	<a
		href="https://wa.me/6285182748023?text=Halo,%20Saya%20akan%20hadir%20di%20acara%20pernikahan%20{namaPria}%20dan%20{namaWanita}"
		target="_blank"
		class="inline-block rounded-lg bg-purple-600 px-6 py-3 text-white shadow-md transition hover:scale-95 hover:bg-purple-800 active:scale-95 active:bg-purple-600 dark:bg-purple-700 dark:hover:bg-purple-600 dark:active:bg-purple-700"
	>
		Konfirmasi via <span class="text-bold text-lg text-green-300 dark:text-green-400">WhatsApp</span
		>
	</a>
</section>
<!-- Hitung Mundur -->
<section class="bg-gray-50 py-8 text-center dark:bg-gray-900">
	<h2 class="mb-4 text-2xl font-bold text-purple-700 dark:text-purple-300">Hitung Mundur Acara</h2>
	<div
		class="mx-auto max-w-xl rounded-xl border border-purple-300 bg-purple-50 p-6 text-lg text-purple-800 shadow transition duration-300 ease-in-out hover:scale-105 dark:border-purple-500 dark:bg-purple-900 dark:text-purple-200"
		bind:this={timerEl}
	>
		Memuat waktu...
	</div>
</section>
<!-- Ucapan & Doa -->
<section
	id="ucapan"
	class="relative overflow-hidden rounded-t-full border-4 border-purple-700 bg-gray-50 px-4 pt-16 pb-10 text-center dark:border-purple-400 dark:bg-gray-900"
>
	<div
		class="absolute inset-0 bg-[url('image/bg-nikah.jpg')] bg-cover bg-center opacity-50 dark:opacity-20"
	></div>

	<div class="relative z-10">
		<h3 class="mb-4 text-xl font-semibold text-purple-800 dark:text-purple-200">Ucapan & Doa</h3>
		<p class="mx-auto max-w-xl text-sm text-gray-800 dark:text-gray-200">
			Semoga pernikahan ini menjadi awal dari kehidupan yang penuh berkah, kebahagiaan, dan cinta
			yang abadi.
		</p>
	</div>
</section>

<!-- Footer -->
<footer id="footer" class="bg-purple-700 py-6 text-center text-white dark:bg-purple-900">
	<p class="mb-4 text-sm">© 2025 Muhammad Andi & Siti Aisyah</p>
	<div class="flex justify-center space-x-4">
		<a href="https://instagram.com/gif_ry02" target="_blank" aria-label="Instagram">
			<svg
				class="h-6 w-6 fill-white transition hover:fill-pink-400 dark:hover:fill-pink-300"
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
				class="h-6 w-6 fill-white transition hover:fill-green-400 dark:hover:fill-green-300"
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
