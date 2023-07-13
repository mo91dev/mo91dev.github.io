<script>
	import { name } from '$lib/constants';
</script>

<main>
	<div class="main-intro container">
		<h1>{name}, LLC</h1>
		<p>
			Welcome to my portfolio! I am an experienced software developer specialized in frontend,
			backend and full stack development.
		</p>
		<a class="cta" href="/portfolio">Check out my work</a>
	</div>
</main>

<style>
	.container {
		width: 80%;
		margin: auto;
		overflow: hidden;
	}

	.main-intro {
		text-align: center;
		padding: 40px 0;
	}

	.main-intro h1 {
		font-size: 45px;
		line-height: 1.3;
	}

	.main-intro p {
		font-size: 24px;
		margin-bottom: 20px;
	}

	.cta {
		background: #2980b9;
		color: white;
		display: inline-block;
		font-size: 20px;
		padding: 10px 20px;
		text-decoration: none;
		border-radius: 5px;
	}

	.cta:hover {
		background: #3498db;
		transition: background 0.2s ease;
	}
</style>
