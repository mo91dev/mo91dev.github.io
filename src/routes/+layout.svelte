<script lang="ts">
	import { name } from '$lib/constants';
	import NavBar from '../components/NavBar.svelte';
	import '../app.css';
</script>

<main>
	<div class="flex h-screen pr-8 pl-8 pb-8">
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
