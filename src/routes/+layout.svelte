<script lang="ts">
	import { name } from '$lib/constants';
	import NavBar from '../components/NavBar.svelte';
</script>

<main class="global">
	<div class="container">
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

<style lang="scss">
	.global {
		display: flex;
		flex-direction: column;
		font-family: 'Arial', sans-serif;
		color: #333;
		background-color: #f4f4f4;
		margin: 0;
		padding: 0px;
		font-size: 1em;
		line-height: 1.5;
	}
	.container {
		min-height: 100vh;
	}
	footer {
		background-color: #cacaca;
		display: flex;
		justify-content: center;
	}
</style>
