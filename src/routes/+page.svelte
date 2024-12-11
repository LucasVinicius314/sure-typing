<script>
	let cards = [
		{ title: 'Card 1', content: 'This is the first card.' },
		{ title: 'Card 2', content: 'This is the second card.' },
		{ title: 'Card 3', content: 'This is the third card.' }
	];
</script>

<div class="flex min-h-screen flex-col bg-gray-100">
	<!-- Navbar -->
	<nav class="bg-white p-4 shadow">
		<div class="container mx-auto flex items-center justify-between">
			<div class="text-lg font-bold">Sure Typing</div>
			<div>
				<a href="#" class="px-3 text-gray-700">Home</a>
				<a href="#" class="px-3 text-gray-700">About</a>
				<a href="#" class="px-3 text-gray-700">Services</a>
				<a href="#" class="px-3 text-gray-700">Contact</a>
			</div>
		</div>
	</nav>

	<!-- Main Content -->
	<main class="container mx-auto flex-grow py-8">
		<h1 class="mb-6 text-3xl font-bold">Welcome to My Page</h1>

		<section class="mb-8">
			<h2 class="mb-4 text-2xl font-semibold">Cards Section</h2>
			<div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
				{#each cards as card}
					<div class="rounded-lg bg-white p-6 shadow">
						<h2 class="mb-2 text-xl font-semibold">{card.title}</h2>
						<p>{card.content}</p>
						<button class="mt-4 rounded bg-blue-500 px-4 py-2 text-white hover:bg-blue-600"
							>More Info</button
						>
					</div>
				{/each}
			</div>
		</section>

		<section class="mb-8">
			<h2 class="mb-4 text-2xl font-semibold">Contact Form</h2>
			<form class="rounded-lg bg-white p-6 shadow">
				<div class="mb-4">
					<label class="mb-2 block text-sm font-bold text-gray-700" for="name">Name</label>
					<input
						class="focus:shadow-outline w-full appearance-none rounded border px-3 py-2 leading-tight text-gray-700 shadow focus:outline-none"
						id="name"
						type="text"
						placeholder="Your Name"
					/>
				</div>
				<div class="mb-4">
					<label class="mb-2 block text-sm font-bold text-gray-700" for="email">Email</label>
					<input
						class="focus:shadow-outline w-full appearance-none rounded border px-3 py-2 leading-tight text-gray-700 shadow focus:outline-none"
						id="email"
						type="email"
						placeholder="Your Email"
					/>
				</div>
				<div class="mb-4">
					<label class="mb-2 block text-sm font-bold text-gray-700" for="message">Message</label>
					<textarea
						class="focus:shadow-outline w-full appearance-none rounded border px-3 py-2 leading-tight text-gray-700 shadow focus:outline-none"
						id="message"
						placeholder="Your Message"
					></textarea>
				</div>
				<button class="rounded bg-green-500 px-4 py-2 text-white hover:bg-green-600">Submit</button>
			</form>
		</section>
	</main>

	<!-- Footer -->
	<footer class="bg-gray-800 p-4 text-white">
		<div class="container mx-auto text-center">
			<p>&copy; 2024 Sure</p>
		</div>
	</footer>
</div>
