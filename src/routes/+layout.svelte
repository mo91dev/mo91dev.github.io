<script lang="ts">
	import { name } from '$lib/constants';
	import NavBar from '../components/NavBar.svelte';
	import '../app.css';
</script>

<main class="">
	<div class="">
		<header>
			<NavBar />
		</header>

		<slot />
		<!-- The content of each individual page goes here -->
	</div>

	<footer>
		<p>&copy; {new Date().getFullYear()} {name}, LLC</p>
	</footer>
</main>

<style lang="postcss">
	:global(a) {
		text-decoration: none;
	}
</style>
