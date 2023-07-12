<main>
    <header>
        <nav>
        <a href="/">Home</a>
        <a href="/portfolio">Portfolio</a>
        <a href="/about">About</a>
        </nav>
    </header>

    <slot></slot> <!-- The content of each individual page goes here -->

    <footer>
        <p>&copy; {new Date().getFullYear()} Mora Ogunro</p>
    </footer>
</main>
  