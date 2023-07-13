<script lang="ts">
	let expanded = false;
	let expandedText = 'Open';
	const expandMenu = (): void => {
		expanded = !expanded;
		expandedText === 'Open' ? (expandedText = 'Close') : (expandedText = 'Open');
		console.log(expanded, expandedText);
	};
</script>

<main>
	<nav class="navbar">
		<a href="/" class="nav-link">Home</a>
		<a href="/portfolio" class="nav-link">Portfolio</a>
		<a href="/about" class="nav-link">About</a>
		<button class="menu-icon" on:click={expandMenu}>
			<i class="fa fa-bars" />
			<p>{expandedText}</p>
		</button>
	</nav>
</main>

<style lang="scss">
</style>
