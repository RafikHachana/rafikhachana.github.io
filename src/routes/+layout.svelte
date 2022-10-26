<script lang="ts">
	import type { HeaderMenuItem } from '$lib/types';

	import Header from '$lib/Header.svelte';
	import Footer from '$lib/Footer.svelte';

	let menu_items: HeaderMenuItem[] = [
		{ text: 'Intro', target: '/' },
		{ text: 'Skills', target: '/#skills' },
		{ text: 'IT Experience', target: '/experience' },
		{ text: 'Contact Me', target: '#contact' },
		{ text: 'About', target: '/about' }
	];
</script>

<div class="app">
	<Header {menu_items} />

	<main>
		<slot />
	</main>

	<Footer />
</div>

<style>
	:global(body) {
		padding: 0px;
		margin: 0px;
		box-shadow: 10px 20px #000000;
		background-color: #aec3b0;
		font-family: 'Poppins', sans-serif;
	}

	main {
		background-color: #eff6e0;
		color: #01161e;
		max-width: 50%;
		margin: auto;
		padding: 2rem;
		text-align: justify;
		margin-bottom: 0px;
	}

	:global(main > section) {
		padding-top: 75px;
	}
</style>
