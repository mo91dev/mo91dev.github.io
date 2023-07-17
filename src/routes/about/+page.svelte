<script>
	let skills = [
		'Java',
		'SpringBoot',
		'React',
		'Svelte',
		'SQL',
		'Full Stack Development',
		'Enterprise Systems'
	];
</script>

<main>
	<h1>About Me</h1>
	<p>
		I'm a software engineer with experience in a variety of technologies. Here are some of my
		skills:
	</p>
	<ul>
		{#each skills as skill (skill)}
			<li>{skill}</li>
		{/each}
	</ul>
</main>
