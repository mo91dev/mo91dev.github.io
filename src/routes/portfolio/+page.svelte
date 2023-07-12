<script>
    let projects = [
      { name: 'Project 1', link: 'https://link-to-project1.com', description: 'Project 1 description' },
      // Add more projects here
    ];
</script>

<main>
    <h1>My Portfolio</h1>
    <ul>
        {#each projects as project (project.name)}
        <li>
            <h2><a href={project.link}>{project.name}</a></h2>
            <p>{project.description}</p>
        </li>
        {/each}
    </ul>
</main>
  