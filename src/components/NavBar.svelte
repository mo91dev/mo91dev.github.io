<script lang="ts">
	import { createMenubar } from '@melt-ui/svelte';
	import { Menu } from 'lucide-svelte';

	const { menubar, createMenu } = createMenubar();
	const { menu, item, trigger } = createMenu();

	import { createToolbar } from '@melt-ui/svelte';

	const { root, button, link, separator, createToolbarGroup } = createToolbar();
	const { root: navGroup, item: navItem } = createToolbarGroup();
</script>

<main>
	<div class="menuMobile" melt={$menubar}>
		<button class="menuButton" melt={$trigger}><Menu /></button>
		<div class="menu" melt={$menu}>
			<button class="item gentle-green" {...$item} use:item>Home</button>
			<button class="item gentle-green" {...$item} use:item>Portfolio</button>
			<button class="item gentle-green" {...$item} use:item>About</button>
		</div>
	</div>

	<div class="desktopNav" melt={$root}>
		<div melt={$navGroup}>
			<button melt={$navItem('bold')}> Home </button>
			<button melt={$navItem('italic')}> Portfolio </button>
			<button melt={$navItem('strikethrough')}> About </button>
		</div>
	</div>
</main>

<style lang="scss">
	.item {
		font-size: 20px;
		border: none;
		padding: 10px 10px 10px 10px;
		margin-left: 0;
		width: 100vw;
		text-align: left;
		display: inline-block;
		border: none;
		background-color: white;
		color: #000;
		text-decoration: none;
		transition: background-color 0.3s ease;

		&:hover {
			background-color: #fff;
			transition: background-color 0.3s ease;
		}

		&.gentle-green {
			&:hover {
				background-color: #eaf5ea;
				transition: background-color 0.3s ease;
			}
		}
	}
	.menuButton {
		border: none;
		width: 40px;
		height: 40px;
	}
	.menu {
		left: 0px !important;
		top: 40px !important;
	}
	.menuMobile {
		@media only screen and (min-width: 768px) {
			display: none; // Hide the button on screens wider than 768px
		}
	}
	.desktopNav {
		@media only screen and (max-width: 768px) {
			display: none; // Hide the button on screens wider than 768px
		}
	}
</style>
